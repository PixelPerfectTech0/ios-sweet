# LG G7 (Adreno 630) GPU userland

Path: Metal -> AdrenoMetal (MIT) -> metal2vulkan -> Turnip (Mesa, MIT) -> NativeAdreno user client -> our A630 kernel driver.

- `mesa-patches/`: Turnip Darwin kernel backend and fixes from UniXNU (https://github.com/UniXNU/UniXNU,
  BSD-2-Clause-Patent, see `LICENSE.UniXNU`), applied in `series` order to Mesa 85fda3b3.
- `abi/NativeAdrenoABI.h`: the kernel/user wire ABI from UniXNU/Adreno740 (MIT, see `LICENSE.NativeAdreno`).
- Built by `.github/workflows/turnip-ios.yml` for iOS 16 arm64.
