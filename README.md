# rsomics-plink-io

PLINK1 binary fileset reader: allele frequency, missingness, Hardy-Weinberg equilibrium, and VCF/012 format export.

## Usage

```
rsomics-plink-io freq    <bfile>   # allele frequency table (plink --freq)
rsomics-plink-io missing <bfile>   # per-variant missingness (plink --missing)
rsomics-plink-io hardy   <bfile>   # Hardy-Weinberg statistics (plink --hardy)
rsomics-plink-io to-vcf  <bfile>   # convert to VCF on stdout
rsomics-plink-io to-012  <bfile>   # dosage matrix (0/1/2) on stdout
```

`<bfile>` is the path prefix for PLINK1 binary filesets (`.bed`, `.bim`, `.fam`).

## Origin

Independent Rust reimplementation of PLINK 1.9 I/O operations based on:

- Chang et al. 2015 (PLINK 1.9, doi:10.1186/s13742-015-0047-8)
- PLINK 1.9 binary fileset format specification: <https://www.cog-genomics.org/plink/1.9/formats>
- Black-box behaviour testing against the `plink` 1.9 binary

No GPL source code from PLINK was used during implementation.
Test fixtures are independently generated using rsomics-pgen's synthetic fixture generator.

License: MIT OR Apache-2.0
Upstream credit: PLINK 1.9 (Christopher Chang et al., GPLv3) — <https://www.cog-genomics.org/plink/>
