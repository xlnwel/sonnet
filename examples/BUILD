package(default_visibility = ["//visibility:private"])

licenses(["notice"])  # Apache 2.0 License

exports_files(["LICENSE"])

load("//sonnet/src:build_defs.bzl", "snt_py_library", "snt_py_test")

py_binary(
    name = "simple_mnist",
    srcs = ["simple_mnist.py"],
    python_version = "PY3",
    srcs_version = "PY2AND3",
    deps = [
        # pip: absl:app
        "//sonnet",
        # pip: tensorflow
        # pip: tensorflow_datasets
        # https://github.com/google/pytype/blob/master/2.7_patches/
    ],
)

snt_py_library(
    name = "simple_mnist_library",
    srcs = ["simple_mnist.py"],
    deps = [
        # pip: absl:app
        "//sonnet",
        # pip: tensorflow
        # pip: tensorflow_datasets
        # https://github.com/google/pytype/blob/master/2.7_patches/
    ],
)

snt_py_test(
    name = "simple_mnist_test",
    srcs = ["simple_mnist_test.py"],
    deps = [
        ":simple_mnist_library",
        "//sonnet",
        "//sonnet/src:test_utils",
        # pip: tensorflow
    ],
)
