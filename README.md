# boost-deptree

Allows for PlantUML visualization of depencencies in boost.

## Dependencies

- python3
- networkx

## Syntax

    python3 deptree.py <boost-root> <out-file> <[--cycle] [--from=<repokey>]>

    where:
      boost-root is the directory of BOOST_ROOT,
      out-file is the name of a file to write PlantUML to

      --cycle shows all direct repository-to-repository cycles
      --from shows all dependencies from the named repository (only direct ones, currently)

Solid lines are compile/runtime dependencies.
Dashed lines are test-only dependencies.

## Samples

### --cycle

![--cycle](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/jeking3/boost-deptree/master/samples/cycles.puml)

### uuid

![--from=uuid](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/jeking3/boost-deptree/master/samples/uuid.puml)
