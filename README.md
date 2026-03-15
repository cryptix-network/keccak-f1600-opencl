# opencl_keccak_f1600

Minimal OpenCL 1.2 implementation of the standard Keccak-f[1600] permutation.

File:
- `opencl_keccak_f1600.cl`

Kernel:
- `keccak_f1600_states_batch`

Input/Output layout:
- one state = `25 * ulong` = `200` bytes
- input buffer = `count * 25` ulongs
- output buffer = `count * 25` ulongs

Build:
- `-cl-std=CL1.2`
- optional define: `-D OPENCL_KECCAK_ALT=1` (default)

Notes:
- This is only the permutation primitive, not SHA3 domain padding/squeezing by itself.
