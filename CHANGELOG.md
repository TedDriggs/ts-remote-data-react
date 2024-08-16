# Changelog

## 0.3.1 (Aug 16, 2024)

- Allow React 17 and 18
- Update `useAsyncOperation` to allow returning `undefined` to mean `RemoteData.NOT_ASKED`. This allows using the hook compatibly with React's exhaustive dependencies lint.
- Eagerly catch rejections in `usePromise` to avoid the browser erroneously believing there are unhandled rejections. If a promise synchronously rejected, the browser would see it before the `useEffect` inside `usePromise` had a chance to register its `catch` callback, resulting in errors showing up in the browser console.


## 0.3.0 (Mar 18, 2020)

- Add hooks which make it easier to work with async actions inside React components (`usePromise`, `usePromiseState`, and `useAsyncOperation`)

## 0.2.1 (May 23, 2019)

- Accept a React node as `failureFallback` for `RemoteSuspense` to better show static errors. [#2](https://github.com/ExtraHop/ts-remote-data-react/pull/2)

## 0.2.0 (May 21, 2019)

- Add `ActivityIndicator` component and hooks.
  This functionality enables background update UI when using `useRemoteLatest`.