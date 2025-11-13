# caretta-id-proto

Protobuf definitions for caretta-id messages.
For Rust implementation and usage examples, see https://github.com/fluo10/caretta-id

## Usage

### Installation

Add this repository to your project.

```bash
git submodule add https://github.com/fluo10/caretta-id-proto
```

### Import

Import and define new message.

```protobuf:foo/bar.proto
syntax = "proto3";
package foo;

import "caretta_id/caretta_id_d.proto";

message Bar {
    caretta_id.CarettaIdD id = 1;
}
```

### Compilation

You must specify the added directory using the `--proto_path` option during compilation.

```bash
protoc --proto_path=caretta-id-proto --python_out=BUILD_DIR foo/bar.proto
```

## License

Licensed under either of:

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE))
- MIT License ([LICENSE-MIT](LICENSE-MIT))

at your option.