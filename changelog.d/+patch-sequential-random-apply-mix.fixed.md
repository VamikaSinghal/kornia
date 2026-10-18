`PatchSequential` with `random_apply` now inserts a mix augmentation such as `RandomMixUpV2` into
the drawn sequence with the same probability as `ImageSequential`, at most once per call. The
mix-insertion step never ran before, so a mix member of a `PatchSequential` was never applied with
`random_apply` although the container documents at most one mix augmentation per call.
