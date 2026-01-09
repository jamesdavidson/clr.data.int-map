# clr.data.int-map

Requires ClojureCLR >= 1.6

## status

Passes test suite but does not implement r/CollFold.

Benchmark suite has not been ported yet.

## install

Download nupkg file from release and add to a local NuGet source then update csproj with

```
<PackageReference Include="clojure.data.int-map" Version="1.3.1-alpha3" />
```

## usage

```
(assembly-load "clojure.data.int-map")
(require '[clojure.data.int-map :as i])
(def s (range 1e6))
(into #{} s)                ; ~100mb
(into (i/int-set) s)        ; ~1mb
(into (i/dense-int-set) s)  ; ~150kb
```

## docs

See https://clojure.github.io/data.int-map

## future

Interop with System.Collections.Generic might be useful.

## license

Copyright © 2026 Zach Tellman, Rich Hickey and contributors

See LICENSE.txt for EPL v1.0
