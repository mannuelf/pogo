# React on Client

This is an example Pogo app with React client-side rendering.

Based on [Simple Server](../simple-server), with the following changes:
 - Added [`index.html`](./index.html), where the app will be rendered on the client
 - Added a [`client`](./client) directory with frontend modules such as [`client/app.jsx`](./client/app.jsx)
 - Added [`client/counter.jsx`](./client/counter.jsx), a counter component that uses `React.useState`

## Run the example

*Make sure [Deno](https://deno.land/) is installed and up to date.*

### Remote

This example cannot be run remotely, because it reads certain files using the filesystem, such as `index.html` and `build/app.js`.

### Local

Alternatively, if you want to play around with the example, run it from a local file:

```sh
curl -fsSL https://github.com/sholladay/pogo/archive/master.tar.gz | tar -xz --strip-components=1 'pogo-master/example'
cd example/react-on-client
mkdir -p build
deno bundle client/app.jsx build/app.js
deno run --allow-net --allow-read run.ts
```

Visit http://localhost:3000/
