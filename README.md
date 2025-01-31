# go-proto-bench (2023)

Decode/Encode Benchmark for Various OSS Go Protocol buffers (proto) Generators

## What's this?

The goal of this repository is to give more data on efficiency and usability of various Protocol Buffers generators and plugins that enhances the native [google.golang.org/protobuf](https://pkg.go.dev/google.golang.org/protobuf) Go de/serialization implementation e.g.:

* [gogoproto](https://github.com/gogo/protobuf) (for v1 proto API)
* [vtprotobuf](https://github.com/planetscale/vtprotobuf) (for v2 API)
* [csprotpo](https://github.com/CrowdStrike/csproto) (for both v1 and v2, but we benchmark only v2 API).

All benchmark code is available for verifications and reproduction.

Benchmarks here use our new [WIP Prometheus Remote Write 2.0](https://github.com/prometheus/prometheus/issues/13105) as a reference protobuf message. What's unique about it, is that we took a high priority on efficiency while developing it which resulted in custom string interning we wished was more popular in the community. 😉

## Results

> NOTE: Performed on MacOS 14.1.1 M1 Pro 16GB RAM

> NOTE2: v1 and v2 refer to Prometheus Remote Write version. You can focus on v2 to see differences between generators.

See early results [here](./prw-bench.results-2023-11-29.txt)

Test result based on Macbook Air M2 macOS 14.3.1 16GB RAM: [here](./prw-bench.results-2024-03-09.txt)
