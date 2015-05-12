# gfx_text

Library for drawing text for [gfx-rs](https://github.com/gfx-rs/gfx-rs) graphics API. Uses [freetype-rs](https://github.com/PistonDevelopers/freetype-rs) underneath.

## Usage

```rust
# Initialize text renderer.
let mut text = gfx_text::new(&mut canvas.factory).unwrap();

# Draw some text 10 pixels down and right from the top left screen corner.
text.draw(
    "The quick brown fox jumps over the lazy dog",  // Text to draw
    [10, 10],                                       // Position
    [0.65, 0.16, 0.16, 1.0],                        // Text color
);

# Render the final batch.
text.draw_end(&mut canvas);
```

*TODO:* Proper docs.

## Examples

See [this example](./examples/styles.rs) on how to draw text in various styles: different sizes, colors, fonts, etc.

## License

* gfx_text licensed under [MIT License](./LICENSE)
* Included by default Noto Sans font uses [Apache License 2.0](./assets/LICENCE.txt)
* Ubuntu Font used in examples has [Ubuntu Font Licence 1.0](./examples/assets/LICENCE.txt)