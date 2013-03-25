use_relative_paths = True

vars = {
  "root_dir": ".",

  "chromium_trunk": "http://src.chromium.org/svn/trunk",
  "chromium_revision": "190304",

  "googlecode_url": "http://%s.googlecode.com/svn",

  "icu_revision": "182486",

  #"libphonenumber_revision": "456",
  #"libvpx_revision": "180104",
}

deps = {
  "../src/media":
    Var("chromium_trunk") + "/src/media@" + Var("chromium_revision"),

  "../src/base":
    Var("chromium_trunk") + "/src/base@" + Var("chromium_revision"),
  "../src/build":
    Var("chromium_trunk") + "/src/build@" + Var("chromium_revision"),
  "../src/google_apis":
    Var("chromium_trunk") + "/src/google_apis@" + Var("chromium_revision"),
  "../src/third_party/libevent":
    Var("chromium_trunk") + "/src/third_party/libevent@" + Var("chromium_revision"),
  "../src/third_party/llvm_build":
    Var("chromium_trunk") + "/src/third_party/llvm_build@" + Var("chromium_revision"),
  "../src/third_party/mach_override":
    Var("chromium_trunk") + "/src/third_party/mach_override@" + Var("chromium_revision"),
  "../src/third_party/modp-b64":
    Var("chromium_trunk") + "/src/third_party/mach_override@" + Var("chromium_revision"),
  "../src/tools/clang":
    Var("chromium_trunk") + "/src/tools/clang@" + Var("chromium_revision"),
  "../src/tools/gyp":
    Var("chromium_trunk") + "/src/tools/gyp@" + Var("chromium_revision"),

  "../src/icu":
    Var("chromium_trunk") + "/deps/third_party/46@182486",

  "../src/tools/gyp":
    (Var("googlecode_url") % "gyp") + "/trunk@1589",
}


deps_os = {
  "win": {
  },
  "ios": {
  },
  "mac": {
  },
  "unix": {
  },
  "android": {
  },
}


include_rules = [
  # Everybody can use some things.
  "+base",
  "+build",
  "+ipc",

  "+testing",
  "+third_party/icu/public",
]


# checkdeps.py shouldn't check include paths for files in these dirs:
skip_child_includes = [
  "testing",
  "third_party",
]


hooks = [
  {
    # Check for landmines (reasons to clobber the build).
    #"pattern": ".",
    #"action": ["python", "src/build/landmines.py"],
  },
]
