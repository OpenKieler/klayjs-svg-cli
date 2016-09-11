klayjs-svg-cli
===
Command line interface for [klayjs-svg](https://github.com/OpenKieler/klayjs-svg).



Usage
===
```
npm install klayjs-svg-cli
```

```
Usage: klayjs-svg-cli.js input.json [...options]
       klayjs-svg-cli.js [...options] [STDIN]

Options:
  -a, --arrows        Add arrow heads to the edges                     [boolean]
  -c, --centerLabels  Centers node labels within their nodes (if not specified
                      differently)                                     [boolean]
  -d, --defs          Definitions to be added to the svg                 [array]
  -n, --noLayout      Does not lay out the input graph, useful if the graph
                      already has been laid out                        [boolean]
  -o, --output        The output file                                   [string]
  -p, --pretty        Pretty prints the svg output                     [boolean]
  -s, --styles        Style to be used                                   [array]
  --help              Show help                                        [boolean]
```

Layout Options
=== 

If global layout options have been used (or should be used) for layout,
wrap the input `graph` and the `options` in a common object:

```
{
  options: { ... },
  graph: { ... }
}
```
The options may be required to create the correct rendering. 
For instance, if the `edgeRouting` is set to `SPLINES`, 
svg `path`s are created instead of `polyline`s. 