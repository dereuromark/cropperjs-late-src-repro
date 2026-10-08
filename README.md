# cropperjs: `<cropper-image>` stays 0×0 when `src` is set after connect

Minimal reproduction for a regression in cropperjs 2.3.0.

Open `index.html` and click **Set src**.

- `?v=2.3.0`: `$ready()` resolves, but `<cropper-image>` stays 0×0.
- `?v=2.2.0`: `<cropper-image>` takes its size (400×300).

The page loads cropperjs from jsDelivr, connects `<cropper-image>` without a `src`, then sets `src` to a generated 800×600 image when you click the button.
