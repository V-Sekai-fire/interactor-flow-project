# interactor-flow-project

A Godot project that exercises the IDTXFlow scene-import addon against the canonical ANNY animation fixture.

## What it is for

Its scenes and scripts import ANNY's animation and blendshape fixtures through the addon and inspect, render and test the result, and the Python scripts regenerate the USD fixture from its source arrays. The fixture's provenance is on the dataset card of `chibifire/anny-anim-fixture`.

## Run

The fixture files are not tracked. Fetch them from the `chibifire/anny-anim-fixture` dataset:

```sh
hf download --repo-type dataset chibifire/anny-anim-fixture \
  anny_anim_fixture.npz anny_anim_fixture.names.json render_test.tscn \
  --local-dir .
hf download --repo-type dataset chibifire/anny-anim-fixture \
  anny_anim_test.usdz anny_anim_test.glb \
  --local-dir art/canonical_anny
```

Then open `project.godot` in the editor. The addon ships Windows binaries only, so the project opens on Windows.

## Licence

MIT; see `LICENSE`.
