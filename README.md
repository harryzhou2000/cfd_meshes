# cfd_meshes — curated test meshes for DNDSR

CGNS mesh files used by the DNDSR C++ and Python test suites.

No LFS — all files are small enough for direct git storage.

| File | Size | Use |
|------|------|-----|
| `UniformSquare_10.cgns` | 32K | Geom pipeline, connectivity, interpolate, distributed read |
| `IV10_10.cgns` | 64K | Geom pipeline, Euler evaluator, Euler restart, distributed read |
| `NACA0012_H2.cgns` | 984K | Geom pipeline, Euler evaluator, distributed read |
| `IV10U_10.cgns` | 72K | Geom pipeline, distributed read (unstructured tri) |
| `Ball2.cgns` | 56M | Geom pipeline [np=8], index conversion (3D mixed-element) |
| `Ball4.cgns` | 6.2M | 3D mixed-element |
| `Uniform32_3D_Periodic.cgns` | 3.1M | Euler evaluator 3D periodic hex |
| `Uniform32_Periodic.cgns` | 112K | Python Geom test |
| `IV10_20.cgns` | 80K | Euler restart redistribute (large) |

## Usage in CI

Clone alongside the DNDSR checkout:

```yaml
- uses: actions/checkout@v4
  with:
    repository: harryzhou2000/cfd_meshes
    path: data/mesh
```
