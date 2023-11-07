# application-artifact

Artifact space of [pythoneda-shared-pythoneda](https://github.com/pythoneda-shared-pythoneda "pythoneda-shared-pythoneda")/[application](https://github.com/pythoneda-shared-pythoneda/application "application").

## How to declare it in your flake

If you are dealing with meta-artifacts, you'd need to check the latest tag of the (meta)artifact of this (artifact) repository: <https://github.com/pythoneda-shared-pythoneda/application-artifact-artifact/tags> and use it instead of the `[version]` placeholder below.

```nix
{
  description = "[..]";
  inputs = rec {
    [..]
    pythoneda-shared-pythoneda-application-artifact = {
      [optional follows]
      url =
        "github:pythoneda-shared-pythoneda/application-artifact-artifact/[version]?dir=application-artifact";
    };
  };
  outputs = [..]
};
```

Should you use another PythonEDA modules, you might want to pin those also used by this project. The same applies to [nixpkgs](https://github.com/nixos/nixpkgs "nixpkgs") and [flake-utils](https://github.com/numtide/flake-utils "flake-utils").

Use the specific package depending on your system (one of `flake-utils.lib.defaultSystems`) and Python version:

- `#packages.[system].pythoneda-shared-pythoneda-application-python38` 
- `#packages.[system].pythoneda-shared-pythoneda-application-python39` 
- `#packages.[system].pythoneda-shared-pythoneda-application-python310` 
- `#packages.[system].pythoneda-shared-pythoneda-application-python311` 

The Nix flake is under the [application-artifact](https://github.com/pythoneda-shared-pythoneda/application-artifact-artifact/tree/main/application-artifact "application-artifact") folder.
