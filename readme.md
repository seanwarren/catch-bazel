Exposes the [Catch](https://github.com/philsquared/Catch) testing framework to
[Bazel](https://bazel.build/).

Add this to your `WORKSPACE` file:

```py
http_archive(
    name = "catch",
    url = "https://github.com/PlacidBox/catch-bazel/archive/v1.9.4.tar.gz",
    strip_prefix = "catch-bazel-1.9.4",
)
```

Then add `@catch//:main` to the `deps` on `cc_test` rules, like:

```py
cc_test(
    name = "my_test",
    srcs = ["my_test.cpp"],
    deps = ["@catch//:main"],
)
```

Use `@catch//:catch` as your dependency  if you need to [write your own main](https://github.com/philsquared/Catch/blob/master/docs/own-main.md#let-catch-take-full-control-of-args-and-config).
This target only exposes the `catch.hpp` header.

See the [example project](https://github.com/PlacidBox/catch-bazel-example) for code-in-action.
