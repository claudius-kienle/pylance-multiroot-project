Reproduce:

0. 
    ```bash
    python -m venv env
    source env/bin/activate
    cd package-1
    pip install -e . --config-settings mode=compat
    ```

1. Open VS Code Workspace `pylance.code-workspace` and navigate to `package-2/package_2/main.py`.
2. Select venv as Python Interpreter
3. Open Quick Fix for `util_function()`
4. It will promp `no code actions available`

PyLance output:

```bash
[Info  - 4:17:29 PM] (19030) Pylance language server 2022.11.40 (pyright 45344736) starting
[Info  - 4:17:29 PM] (19030) Server root directory: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist
[Info  - 4:17:29 PM] (19030) Starting service instance "package-1"
[Info  - 4:17:29 PM] (19030) Starting service instance "package-2"
[Info  - 4:17:29 PM] (19030) Notebook support: LSP
[Info  - 4:17:29 PM] (19030) Interactive window support: LSP
[Info  - 4:17:29 PM] (19030) Starting service instance "<default>"
[Info  - 4:17:29 PM] (19030) No pyproject.toml file found.
[Info  - 4:17:29 PM] (19030) Setting pythonPath for service "<default>": "~/Documents/Programmieren/develop/pylance-test/env/bin/python"
[Warn  - 4:17:29 PM] (19030) stubPath typings is not a valid directory.
[Info  - 4:17:29 PM] (19030) Assuming Python version 3.10
[Info  - 4:17:29 PM] (19030) Assuming Python platform Linux
[Info  - 4:17:29 PM] (19030) Search paths for <default>
[Info  - 4:17:29 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib
[Info  - 4:17:29 PM] (19030)   typings
[Info  - 4:17:29 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stubs/...
[Info  - 4:17:29 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/bundled/stubs
[Info  - 4:17:29 PM] (19030)   /usr/lib/python3.10
[Info  - 4:17:29 PM] (19030)   /usr/lib/python3.10/lib-dynload
[Info  - 4:17:29 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
[Info  - 4:17:29 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:29 PM] (19030) Searching for source files
[Info  - 4:17:29 PM] (19030) No source files found.
(19030) [IDX(FG)] index libraries  (index) ...
(19030) [IDX(FG)]   read stdlib indices (30ms)
(19030) [IDX(FG)] index libraries  (index) [succeed] (34ms)
(19030) [FG] parsing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (37ms)
(19030) [FG] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi [fs read 3ms] (153ms)
(19030) [FG] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi (34ms)
(19030) [FG] binding: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
[Info  - 4:17:30 PM] (19030) Background analysis(1) root directory: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist
[Info  - 4:17:30 PM] (19030) Background analysis(1) started
[Info  - 4:17:30 PM] (19030) Background analysis(2) root directory: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist
[Info  - 4:17:30 PM] (19030) Background analysis(2) started
[Info  - 4:17:30 PM] (19030) Background analysis(3) root directory: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist
[Info  - 4:17:30 PM] (19030) Background analysis(3) started
(19030) Background analysis message: setConfigOptions
(19030) Background analysis message: setImportResolver
(19030) Background analysis message: ensurePartialStubPackages
(19030) Background analysis message: setTrackedFiles
(19030) Background analysis message: markAllFilesDirty
(19030) Background analysis message: setFileOpened
(19030) Background analysis message: setFileOpened
(19030) Background analysis message: getDiagnosticsForRange
(19030) Background analysis message: analyze
[Info  - 4:17:30 PM] (19030) No configuration file found.
[Info  - 4:17:30 PM] (19030) pyproject.toml file found at ~/Documents/Programmieren/develop/pylance-test/package-1.
[Info  - 4:17:30 PM] (19030) Setting pythonPath for service "package-1": "~/Documents/Programmieren/develop/pylance-test/env/bin/python"
[Info  - 4:17:30 PM] (19030) Loading pyproject.toml file at ~/Documents/Programmieren/develop/pylance-test/package-1/pyproject.toml
[Error - 4:17:30 PM] (19030) Pyproject file "~/Documents/Programmieren/develop/pylance-test/package-1/pyproject.toml" is missing "[tool.pyright]" section.
[Warn  - 4:17:30 PM] (19030) stubPath ~/Documents/Programmieren/develop/pylance-test/package-1/typings is not a valid directory.
[Info  - 4:17:30 PM] (19030) Assuming Python version 3.10
[Info  - 4:17:30 PM] (19030) Assuming Python platform Linux
[Info  - 4:17:30 PM] (19030) Search paths for ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1/typings
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stubs/...
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/bundled/stubs
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10/lib-dynload
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030) Adding fs watcher for library directories:
 /usr/lib/python3.10
/usr/lib/python3.10/lib-dynload
~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
[Info  - 4:17:30 PM] (19030) Adding fs watcher for directories:
 ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030) Searching for source files
[Info  - 4:17:30 PM] (19030) Found 3 source files
(19030) Background analysis message: setConfigOptions
(19030) Background analysis message: setImportResolver
(19030) Background analysis message: ensurePartialStubPackages
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py ...
(19030) [BG(3)]   parsing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (41ms)
[Info  - 4:17:30 PM] (19030) No configuration file found.
[Info  - 4:17:30 PM] (19030) pyproject.toml file found at ~/Documents/Programmieren/develop/pylance-test/package-2.
[Info  - 4:17:30 PM] (19030) Setting pythonPath for service "package-2": "~/Documents/Programmieren/develop/pylance-test/env/bin/python"
[Info  - 4:17:30 PM] (19030) Loading pyproject.toml file at ~/Documents/Programmieren/develop/pylance-test/package-2/pyproject.toml
[Error - 4:17:30 PM] (19030) Pyproject file "~/Documents/Programmieren/develop/pylance-test/package-2/pyproject.toml" is missing "[tool.pyright]" section.
[Warn  - 4:17:30 PM] (19030) stubPath ~/Documents/Programmieren/develop/pylance-test/package-2/typings is not a valid directory.
[Info  - 4:17:30 PM] (19030) Assuming Python version 3.10
[Info  - 4:17:30 PM] (19030) Assuming Python platform Linux
[Info  - 4:17:30 PM] (19030) Search paths for ~/Documents/Programmieren/develop/pylance-test/package-2
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-2
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-2/typings
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stubs/...
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/bundled/stubs
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10/lib-dynload
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030) Adding fs watcher for library directories:
 /usr/lib/python3.10
/usr/lib/python3.10/lib-dynload
~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030) Adding fs watcher for directories:
 ~/Documents/Programmieren/develop/pylance-test/package-2
[Info  - 4:17:30 PM] (19030) Searching for source files
[Info  - 4:17:30 PM] (19030) Found 2 source files
(19030) Background analysis message: setConfigOptions
(19030) Background analysis message: setImportResolver
(19030) Background analysis message: ensurePartialStubPackages
[Info  - 4:17:30 PM] (19030) No pyproject.toml file found.
[Info  - 4:17:30 PM] (19030) Setting pythonPath for service "<default>": "~/Documents/Programmieren/develop/pylance-test/env/bin/python"
[Warn  - 4:17:30 PM] (19030) stubPath typings is not a valid directory.
[Info  - 4:17:30 PM] (19030) Assuming Python version 3.10
[Info  - 4:17:30 PM] (19030) Assuming Python platform Linux
[Info  - 4:17:30 PM] (19030) Search paths for <default>
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib
[Info  - 4:17:30 PM] (19030)   typings
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stubs/...
[Info  - 4:17:30 PM] (19030)   ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/bundled/stubs
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10
[Info  - 4:17:30 PM] (19030)   /usr/lib/python3.10/lib-dynload
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/env/lib/python3.10/site-packages
[Info  - 4:17:30 PM] (19030)   ~/Documents/Programmieren/develop/pylance-test/package-1
[Info  - 4:17:30 PM] (19030) Searching for source files
[Info  - 4:17:30 PM] (19030) No source files found.
(19030) [IDX(FG)] index libraries  (index) ...
(19030) [IDX(FG)]   read stdlib indices (0ms)
(19030) [IDX(FG)] index libraries  (index) [succeed] (4ms)
(19030) Background analysis message: setTrackedFiles
(19030) Background analysis message: markAllFilesDirty
(19030) Background analysis message: analyze
(19030) [FG] parsing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py [fs read 1ms] (11ms)
(19030) [FG] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi [fs read 0ms] (68ms)
(19030) [FG] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi (23ms)
(19030) [FG] binding: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
(19030) Background analysis message: setTrackedFiles
(19030) Background analysis message: markAllFilesDirty
(19030) Background analysis message: analyze
(19030) [BG(3)]   parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi [fs read 2ms] (138ms)
(19030) [BG(3)]   binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi (24ms)
(19030) [BG(3)]   binding: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (0ms)
(19030) [BG(3)]   checking: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (4ms)
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (208ms)
(19030) Background analysis message: getDiagnosticsForRange
(19030) Background inlayHint message
(19030) [BG(3)] parsing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (1ms)
(19030) [BG(3)] binding: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
(19030) [BG(3)] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing.pyi [fs read 1ms] (26ms)
(19030) [BG(3)] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing.pyi (6ms)
(19030) [BG(3)] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing_extensions.pyi [fs read 0ms] (3ms)
(19030) [BG(3)] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing_extensions.pyi (2ms)
(19030) [FG] parsing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (23ms)
(19030) [FG] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi [fs read 0ms] (73ms)
(19030) [FG] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi (26ms)
(19030) [FG] binding: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
(19030) [BG(3)] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/_typeshed/__init__.pyi [fs read 0ms] (24ms)
(19030) [BG(3)] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/_typeshed/__init__.pyi (2ms)
(19030) [BG(3)] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/types.pyi [fs read 0ms] (6ms)
(19030) [BG(3)] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/types.pyi (2ms)
(19030) [BG(3)] parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/abc.pyi [fs read 0ms] (1ms)
(19030) [BG(3)] binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/abc.pyi (0ms)
(19030) Background analysis message: getSemanticTokens full
(19030) [BG(3)] getSemanticTokens full at ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (2ms)
(19030) Background analysis message: getSemanticTokens full
(19030) [BG(3)] getSemanticTokens full at ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (3ms)
(19030) Background analysis message: setConfigOptions
(19030) Background analysis message: setImportResolver
(19030) Background analysis message: ensurePartialStubPackages
(19030) Background analysis message: setTrackedFiles
(19030) Background analysis message: markAllFilesDirty
(19030) Background analysis message: analyze
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py ...
(19030) [BG(3)]   parsing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (23ms)
(19030) [BG(3)]   parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi [fs read 0ms] (100ms)
(19030) [BG(3)]   binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/builtins.pyi (17ms)
(19030) [BG(3)]   binding: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (0ms)
(19030) [BG(3)]   checking: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py ...
(19030) [BG(3)]     parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing.pyi [fs read 1ms] (22ms)
(19030) [BG(3)]     binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing.pyi (2ms)
(19030) [BG(3)]     parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing_extensions.pyi [fs read 0ms] (3ms)
(19030) [BG(3)]     binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/typing_extensions.pyi (1ms)
(19030) [BG(3)]     parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/_typeshed/__init__.pyi [fs read 0ms] (21ms)
(19030) [BG(3)]     binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/_typeshed/__init__.pyi (0ms)
(19030) [BG(3)]     parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/types.pyi [fs read 1ms] (4ms)
(19030) [BG(3)]     binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/types.pyi (2ms)
(19030) [BG(3)]     parsing: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/abc.pyi [fs read 0ms] (1ms)
(19030) [BG(3)]     binding: ~/.vscode/extensions/ms-python.vscode-pylance-2022.11.40/dist/typeshed-fallback/stdlib/abc.pyi (0ms)
(19030) [BG(3)]   checking: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (68ms)
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-1/util_package/functions.py (209ms)
(19030) Background analysis message: resumeAnalysis
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py ...
(19030) [BG(3)]   parsing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
(19030) [BG(3)]   binding: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (0ms)
(19030) [BG(3)]   checking: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (3ms)
(19030) [BG(3)] analyzing: ~/Documents/Programmieren/develop/pylance-test/package-2/package_2/main.py (3ms)
(19030) Background analysis message: resumeAnalysis
(19030) Background analysis message: getDiagnosticsForRange
(19030) Background analysis message: getDiagnosticsForRange
```