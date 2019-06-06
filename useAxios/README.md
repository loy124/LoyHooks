# @loyhooks/use-axios

React Hook to execute a function when axios

## Installation

#### yarn

`yarn add @loyhooks/use-axios`

#### npm

`npm i @loyhooks/use-axios`

## Usage

```js
import React from "react";
import useBeforeLeave from "@loyhooks/use-axios";

const App = () => {
  const { loading, data, error, refetch } = useAxios({
    url: "https://yts.am/api/v2/list_movies.json"
  });
  console.log(
    `Loading:${loading}\nError:${error}\nData:${JSON.stringify(data)}`
  );
  return (
    <div className="App">
      <h1>{data && data.status}</h1>
      <h2> {loading && "Loading"}</h2>
      <button onClick={refetch}>Refetch</button>
    </div>
  );
};

```

### Arguments

| Argument      | Type     | Description                                              | Required |
| ------------- | -------- | -------------------------------------------------------- | -------- |
| onBeforeLeave | function | Function to be called when the mouse leaves the document | yes      |
