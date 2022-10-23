
-   [`configureStore()`](https://redux-toolkit.js.org/api/configureStore): wraps  `createStore`  to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes  `redux-thunk`  by default, and enables use of the Redux DevTools Extension.
-   [`createReducer()`](https://redux-toolkit.js.org/api/createReducer): that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the  [`immer`  library](https://github.com/immerjs/immer)  to let you write simpler immutable updates with normal mutative code, like  `state.todos[3].completed = true`.
-   [`createAction()`](https://redux-toolkit.js.org/api/createAction): generates an action creator function for the given action type string. The function itself has  `toString()`  defined, so that it can be used in place of the type constant.
-   [`createSlice()`](https://redux-toolkit.js.org/api/createSlice): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
-   [`createAsyncThunk`](https://redux-toolkit.js.org/api/createAsyncThunk): accepts an action type string and a function that returns a promise, and generates a thunk that dispatches  `pending/fulfilled/rejected`  action types based on that promise
-   [`createEntityAdapter`](https://redux-toolkit.js.org/api/createEntityAdapter): generates a set of reusable reducers and selectors to manage normalized data in the store
-   The  [`createSelector`  utility](https://redux-toolkit.js.org/api/createSelector)  from the  [Reselect](https://github.com/reduxjs/reselect)  library, re-exported for ease of use.


## RTK Query[​](https://redux-toolkit.js.org/introduction/getting-started#rtk-query "Direct link to heading")

[**RTK Query**](https://redux-toolkit.js.org/rtk-query/overview)  is provided as an optional addon within the  `@reduxjs/toolkit`  package. It is purpose-built to solve the use case of data fetching and caching, supplying a compact, but powerful toolset to define an API interface layer for your app. It is intended to simplify common cases for loading data in a web application, eliminating the need to hand-write data fetching & caching logic yourself.



RTK Query includes these APIs:

-   [`createApi()`](https://redux-toolkit.js.org/rtk-query/api/createApi): The core of RTK Query's functionality. It allows you to define a set of endpoints describe how to retrieve data from a series of endpoints, including configuration of how to fetch and transform that data. In most cases, you should use this once per app, with "one API slice per base URL" as a rule of thumb.
-   [`fetchBaseQuery()`](https://redux-toolkit.js.org/rtk-query/api/fetchBaseQuery): A small wrapper around  [`fetch`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)  that aims to simplify requests. Intended as the recommended  `baseQuery`  to be used in  `createApi`  for the majority of users.
-   [`<ApiProvider />`](https://redux-toolkit.js.org/rtk-query/api/ApiProvider): Can be used as a  `Provider`  if you  **do not already have a Redux store**.
-   [`setupListeners()`](https://redux-toolkit.js.org/rtk-query/api/setupListeners): A utility used to enable  `refetchOnMount`  and  `refetchOnReconnect`  behaviors.
