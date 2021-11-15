load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "2.5"

RULES_JVM_EXTERNAL_SHA = "249e8129914be6d987ca57754516be35a14ea866c616041ff0cd32ea94d2f3a1"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "com.google.inject:guice:5.0.1",
        "com.google.inject.extensions:guice-servlet:5.0.1",
        "com.google.inject.extensions:guice-persist:5.0.1",

        "org.eclipse.jetty:jetty-servlet:11.0.7",
        "org.eclipse.jetty:jetty-server:11.0.7",
        "org.eclipse.jetty:jetty-util:11.0.7",
        "javax.servlet:javax.servlet-api:4.0.1",
        "jakarta.servlet:jakarta.servlet-api:5.0.0",

        "org.apache.commons:commons-lang3:3.9",
        "junit:junit:4.13.2",
    ],
    repositories = [
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
)
