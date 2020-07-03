---
title: "Save a value in persistent storage with useReducer"
layout: post
date: 2020-07-02 21:40
lang: English
ref: useLocalStorage
image: /assets/images/reacthooks.png
headerImage: true
tag:
- react
- javascript
- typescript
star: false
category: blog
author: joe
description: Save a value in persistent storage with useReducer
---

React doesn't provide a hook to store state in persistent storage such as `localStorage`.
For a simple state, we can adopt the [useLocalStorage](https://usehooks.com/useLocalStorage/) provided by the [usehooks](https://usehooks.com/) website. It wraps the `useState` hook.

However, how about a complicated object? It would be better to wrap the `useReducer` hook. 
Here is my implementation. The `dataProvider` is an abstraction of the persistent storage. For example, if we want to use `localStorage`, then just replace it with the APIs of `localStorage`.

---

{% highlight js %}
export const usePersistentStorage = (update, initialStorage, storageKey, dataProvider, init = null) => {

	const [storage, dispatch] = React.useReducer(update, initialStorage, (initialState) => {
        const persistentStorage = dataProvider.getData(storageKey);

        if (persistentStorage !== null) {
            return persistentStorage;
        } else if (init !== null) {
            return init(initialState);
        } else {
            return initialState;
        }
    });
	
	dataProvider.setData(storageKey, storage);
	return [storage, dispatch];
}
{% endhighlight %}
