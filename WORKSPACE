# workspace(name = "js_image_oci")
#
# load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
#
# # http_archive(
# #     name = "aspect_rules_js",
# #     sha256 = "7ab2fbe6d79fb3909ad2bf6dcacfae39adcb31c514efa239dd730b4f147c8097",
# #     strip_prefix = "rules_js-1.32.1",
# #     url = "https://github.com/aspect-build/rules_js/releases/download/v1.32.1/rules_js-v1.32.1.tar.gz",
# # )
# #
# # load("@aspect_rules_js//js:repositories.bzl", "rules_js_dependencies")
# #
# # rules_js_dependencies()
# #
# # load("@rules_nodejs//nodejs:repositories.bzl", "DEFAULT_NODE_VERSION", "nodejs_register_toolchains")
# #
# # nodejs_register_toolchains(
# #     name = "nodejs",
# #     node_version = DEFAULT_NODE_VERSION,
# # )
#
# # For convenience, npm_translate_lock does this call automatically.
# # Uncomment if you don't call npm_translate_lock at all.
# #load("@bazel_features//:deps.bzl", "bazel_features_deps")
# #bazel_features_deps()
#
# # load("@aspect_rules_js//npm:repositories.bzl", "npm_translate_lock")
# #
# # npm_translate_lock(
# #     name = "npm",
# #     pnpm_lock = "//:pnpm-lock.yaml",
# #     verify_node_modules_ignored = "//:.bazelignore",
# # )
# #
# # load("@npm//:repositories.bzl", "npm_repositories")
# #
# # npm_repositories()
#
# http_archive(
#     name = "aspect_rules_ts",
#     sha256 = "4c3f34fff9f96ffc9c26635d8235a32a23a6797324486c7d23c1dfa477e8b451",
#     strip_prefix = "rules_ts-1.4.5",
#     url = "https://github.com/aspect-build/rules_ts/releases/download/v1.4.5/rules_ts-v1.4.5.tar.gz",
# )
#
# ##################
# # rules_ts setup #
# ##################
# # Fetches the rules_ts dependencies.
# # If you want to have a different version of some dependency,
# # you should fetch it *before* calling this.
# # Alternatively, you can skip calling this function, so long as you've
# # already fetched all the dependencies.
# load("@aspect_rules_ts//ts:repositories.bzl", "rules_ts_dependencies", "LATEST_TYPESCRIPT_VERSION")
#
# rules_ts_dependencies(
#     # This keeps the TypeScript version in-sync with the editor, which is typically best.
#     # ts_version_from = "//src:package.json",
#
#     # Alternatively, you could pick a specific version, or use
#     # load("@aspect_rules_ts//ts:repositories.bzl", "LATEST_TYPESCRIPT_VERSION")
#     ts_version = LATEST_TYPESCRIPT_VERSION
# )
#
# # Fetch and register node, if you haven't already
# load("@rules_nodejs//nodejs:repositories.bzl", "DEFAULT_NODE_VERSION", "nodejs_register_toolchains")
#
# nodejs_register_toolchains(
#     name = "node",
#     node_version = DEFAULT_NODE_VERSION,
# )
#
# # Register aspect_bazel_lib toolchains;
# # If you use npm_translate_lock or npm_import from aspect_rules_js you can omit this block.
# load("@aspect_bazel_lib//lib:repositories.bzl", "register_copy_directory_toolchains", "register_copy_to_directory_toolchains")
#
# register_copy_directory_toolchains()
#
# register_copy_to_directory_toolchains()
#
# ###
# # Setup rules_oci
# ###
#
# http_archive(
#     name = "rules_oci",
#     # sha256 = "08d73a9bec22642ee12c0a38c23596cbddaba7422eede74edba3bb1044d579be",
#     strip_prefix = "rules_oci-1.3.1",
#     url = "https://github.com/bazel-contrib/rules_oci/releases/download/v1.3.1/rules_oci-v1.3.1.tar.gz",
# )
#
# load("@rules_oci//oci:dependencies.bzl", "rules_oci_dependencies")
#
# rules_oci_dependencies()
#
# load("@rules_oci//oci:repositories.bzl", "LATEST_CRANE_VERSION", "oci_register_toolchains")
#
# oci_register_toolchains(
#     name = "oci",
#     crane_version = LATEST_CRANE_VERSION,
# )
#
# ## Pull base images
# load("@rules_oci//oci:pull.bzl", "oci_pull")
#
# oci_pull(
#     name = "debian",
#     digest = "sha256:3d868b5eb908155f3784317b3dda2941df87bbbbaa4608f84881de66d9bb297b",
#     image = "debian",
#     platforms = [
#         "linux/386",
#         "linux/amd64",
#         "linux/arm/v5",
#         "linux/arm/v7",
#         "linux/arm64/v8",
#         "linux/mips64le",
#         "linux/ppc64le",
#         "linux/s390x",
#     ],
# )
#
