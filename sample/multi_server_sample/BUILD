load("@protobuf//:protobuf.bzl", "cc_proto_library")

cc_proto_library(
  name = "echo_proto",
  srcs = [
    "echo_service.proto",
  ],
  include = ".",
  default_runtime = "@protobuf//:protobuf",
  protoc = "@protobuf//:protoc",
)

cc_binary(
  name = "server",
  srcs = ["server.cc"],

  deps = [
    ":echo_proto",
    "//:sofa-pbrpc",
    "@protobuf//:protobuf",
    "@protobuf//:protoc_lib",
  ],
  visibility = ["//main:__pkg__"],
)

cc_binary(
  name = "client",
  srcs = ["client.cc"],

  deps = [
    ":echo_proto",
    "//:sofa-pbrpc",
    "@protobuf//:protobuf",
    "@protobuf//:protoc_lib",
  ],
  visibility = ["//main:__pkg__"],
)
