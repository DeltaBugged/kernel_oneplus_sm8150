SUSFS Linux 4.14 integration sources

The patch is the 4.14 port from JackA1ltman/NonGKI_Kernel_Build_2nd:
- Patches/Patch/susfs_patch_to_4.14.patch (blob 2e9a5947657ddd75e19e4bacbe3d12e01c152666)
- Patches/susfs_inline_hook_patches.sh (blob 250d004b0010f29cca73c6f52fab926197877aea)

The patch declares SUSFS_VERSION "v2.4.0". The accompanying script labels its hook API level 2.3.00; the kernel-side patch version is authoritative for this integration.

The inline-hook script is adapted for this BakaSU revision: ksu_handle_sys_read() is called with its actual (fd, buf_ptr, count_ptr) arguments. Hook integration is performed after the SUSFS filesystem patch. The upstream script's whole-file KernelSU skip guard is retained; the workflow applies the script before introducing any manual hook calls, so it does not silently skip those files.

The user has confirmed they have the necessary rights to incorporate and relicense these contributions for this repository. Preserve the original upstream author credits in the source files.
