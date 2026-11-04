# Lab report: safety-for-agentic-ai

- **Upstream:** [NVIDIA-AI-Blueprints/safety-for-agentic-ai](https://github.com/NVIDIA-AI-Blueprints/safety-for-agentic-ai) (Apache-2.0)
- **Run:** 2026-11-04 (new)
- **Stack:** python
- **Build:** failing

## Steps

| Step | Result | Time |
|---|---|---|
| venv tools | ok | 3.8s |
| pip install | FAILED | 1.6s |
| new test lab_tests/test_repository_smoke.py | ok | 0.4s |

## Generated tests

- `lab_tests/test_repository_smoke.py` (2 passing)

## Improvement

No improvement landed this run.

## Logs of failed steps

### pip install
```
  error: subprocess-exited-with-error
  
  × Preparing metadata (pyproject.toml) did not run successfully.
  │ exit code: 1
  ╰─> [17 lines of output]
      Traceback (most recent call last):
        File "/home/runner/work/_temp/lab-build/venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 406, in <module>
          main()
        File "/home/runner/work/_temp/lab-build/venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 381, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/runner/work/_temp/lab-build/venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 181, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-u7ilhb6h/overlay/lib/python3.12/site-packages/poetry/core/masonry/api.py", line 43, in prepare_metadata_for_build_wheel
          builder = WheelBuilder(poetry, config_settings=config_settings)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-u7ilhb6h/overlay/lib/python3.12/site-packages/poetry/core/masonry/builders/wheel.py", line 67, in __init__
          super().__init__(poetry, executable=executable, config_settings=config_settings)
        File "/tmp/pip-build-env-u7ilhb6h/overlay/lib/python3.12/site-packages/poetry/core/masonry/builders/builder.py", line 40, in __init__
          raise RuntimeError(
      RuntimeError: Building a package is not possible in non-package mode.
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> from file:///home/runner/work/_temp/lab-build/tree

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.

```
