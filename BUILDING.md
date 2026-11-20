# Building the hotdogb KernelSU + SUSFS kernel

The GitHub Actions workflow `.github/workflows/build-kernel.yml` builds the ARM64
`Image.gz-dtb` using `vendor/sm8150-perf_defconfig`.

The workflow checks that KernelSU, SUSFS, Kprobes, and Kretprobes are enabled,
then compiles the kernel and uploads `Image.gz-dtb`, `vmlinux`, `System.map`,
and the generated kernel configuration as a 14-day Actions artifact.

Run it from the Actions tab with the `Build KernelSU SUSFS kernel` workflow,
or push a change to this file or the build workflow on `ksu-susfs`.
