
## Docker
Install [docker](https://www.docker.com/) and run:

```bash
docker build -t jgfdot .
cat example/graph.json | docker run --rm --interactive jgfdot
```

## Javascript API

You can also use the programmatic API to convert json graph objects to dot file strings

```js
var toDot = require("jgf-dot");

var graph = require("./graph.json");

var fs = require("fs");

var dot = toDot(graph);

fs.writeFileSync("graph.dot", dot, "utf8");
```

**NOTE:** Currently the graph isn't being valdated before it gets parsed, but that feature is on the todo list.
