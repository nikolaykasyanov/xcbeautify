load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

git_repository(
    name = "build_bazel_rules_swift",
    commit = "410d8ed546e3e43dd06f01cb3916ede6632a6d71",
    remote = "https://github.com/bazelbuild/rules_swift.git",
)

load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

load(
    "@com_google_protobuf//:protobuf_deps.bzl",
    "protobuf_deps",
)

protobuf_deps()

http_archive(
    name = "Colorizer",
    build_file = "//external:External.BUILD",
    sha256 = "267aff5c4a6a7c7f329ca96b2d5683f17098b3cee859e01e96a77e2d08805750",
    strip_prefix = "Colorizer-0.2.1",
    url = "https://github.com/getGuaka/Colorizer/archive/0.2.1.zip",
)

http_archive(
    name = "ArgumentParser",
    build_file = "//external:External.BUILD",
    sha256 = "a79951e4783a7265b54cf216a64b5cd751568da9606c8980a9afa89c5f06d21f",
    strip_prefix = "swift-argument-parser-0.5.0",
    url = "https://github.com/apple/swift-argument-parser/archive/0.5.0.zip",
)
