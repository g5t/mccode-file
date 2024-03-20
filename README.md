# McCode File component
A component to write a file based on the contents of a `METADATA` entry.

## Usage

```c
COMPONENT file_instance_name = File(filename="off_file.off", metadatakey="file_instance_name:metadata_entry_name") AT (0, 0, 0)
METADATA metadata_entry_name "mimetype/text" %{OFF
8 6
0.0 0.0 0.0
0.0 1.0 0.0
0.0 1.0 1.0
0.0 0.0 1.0
1.0 0.0 0.0
1.0 1.0 0.0
1.0 1.0 1.0
1.0 0.0 1.0
4 0 3 2 1
4 4 5 6 7
4 0 1 6 5
4 3 6 7 2
4 3 0 4 7
4 1 2 5 6
%}
```

or 

```c
COMPONENT some_arm = Arm() AT (x, y, z) ...
METADATA some_name "mimetype/JSON" %{{"some_value": 14, "has_name": false}%}

COMPONENT file_instance = File(metadatakey="some_arm:some_name") AT (0, 0, 0);
```
