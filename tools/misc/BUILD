filegroup(
    name = "wrapper_script",
    srcs = ["pleasew"],
    visibility = ["PUBLIC"],
)

filegroup(
    name = "completion_script",
    srcs = ["plz_complete.sh"],
    visibility = ["PUBLIC"],
)

python_binary(
    name = "gen_release",
    labels = ["hlink:plz-out/pkg"],
    main = "gen_release.py",
    deps = [
        "//:changelog",
        "//:version",
        "//third_party/python:absl",
        "//third_party/python:colorlog",
        "//third_party/python:requests",
    ],
)
