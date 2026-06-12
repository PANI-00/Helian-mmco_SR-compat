# Helian-mmco_SR-compat

**Helian-mmco (Sundial Lite edit) — Super Resolution Compatible**

基于 [MoAoXnX/Helian-mmco_Sundial-Lite_edit](https://github.com/MoAoXnX/Helian-mmco_Sundial-Lite_edit) 修改，增加了 [Super Resolution](https://github.com/187J3X1-114514/superresolution) 模组的兼容支持。

Super Resolution compatibility patch for Helian-mmco, based on [MoAoXnX/Helian-mmco_Sundial-Lite_edit](https://github.com/MoAoXnX/Helian-mmco_Sundial-Lite_edit) with [Super Resolution](https://github.com/187J3X1-114514/superresolution) mod support.

---

## 🚀 Super Resolution

Super Resolution 是一个 Minecraft 模组，通过 **FSR / DLSS / XeSS** 等超分辨率技术，在几乎不损失画质的情况下大幅提升帧率：用更低的内部分辨率渲染，通过算法智能放大到目标分辨率，从而获得更高的 FPS，而画面损失几乎不可察觉。

Super Resolution is a Minecraft mod that uses **FSR / DLSS / XeSS** upscaling to significantly boost FPS with nearly no visual quality loss — renders at a lower internal resolution, then intelligently upscales to your target resolution.

详细功能介绍和配置说明请见：[Super Resolution 模组仓库](https://github.com/187J3X1-114514/superresolution)

For detailed features and configuration, visit: [Super Resolution Mod Repository](https://github.com/187J3X1-114514/superresolution)

---

## 📦 安装 / Installation

1. 安装 [Super Resolution](https://github.com/187J3X1-114514/superresolution) 模组（NeoForge / Fabric）
2. 将本光影包放入 `.minecraft/shaderpacks/` 目录
3. 在游戏中选中本光影包，SR 配置会自动生效

1. Install the [Super Resolution](https://github.com/187J3X1-114514/superresolution) mod (NeoForge / Fabric)
2. Place this shaderpack in your `.minecraft/shaderpacks/` folder
3. Select it in-game — the SR configuration will activate automatically

---

# Helian-MMCO (Sundial lite edit)

Personal simple modification of Sundial-lite.
(Helian/Helianthus)
![6748](https://github.com/user-attachments/assets/620e4f18-51cb-493a-a4b5-cf4138a30aad)

# Sundial Lite

Sundial Lite is the free and open source version of Sundial, using [GNU General Public Licence 3.0](./LICENSE). It's designed to make the balance between quality, performance and compatibility. For the full version which is still not complete and need subscription for early testing versions, visit [Aifadian](https://afdian.com/a/geforcelegend). For legit issues, I'll try avoid using platforms blocked by GFW like Patreon, so sorry for some users having issue signing in this site.

## Supported versions

Optifine released after 04.12.2019 (1.8.9 L5) is supported.

Theoretically can run on Iris 1.5.0 and above, but for less bugs, latest Iris is suggested.

## Features

Sundial Lite contains most features from the full version and with some extra features, including but not limits to:

- Shadowmapping, including transparent shadow and water caustics
- Waving plants
- Full LabPBR support (LabPBR AO is disabled by default) and some optional builtin PBR material for certain blocks
- Builtin anisotropic filtering, does not need vanilla/Optifine's anisotropic enabled
- Smooth parallax for smoothed surface, and voxel parallax for exact cubic surface
- Parallax based normal for unified parallax and normal experience
- Percentage closer soft shadow, screen space shadow and cloud shadow
- Noisy SSGI and SSAO based on [screen space visibility bitmask from shadertoy (CC0)](https://www.shadertoy.com/view/XcdBWf)
- Screen space reflection with reflection filter
- Physical based atmosphere that considers player height
- Switchable blocky and realistic cloud, both can occlude ground if you fly high enough, and extra 2D plane cloud
- Vanilla weather rendering
- Switchable realistic and vanilla style water type
- Refraction based on one time offset
- Sunlight specular on transparent objects
- Water fog, nether fog and the end fog, also include galaxy for the end
- Volumetric light and volumetric fog
- Depth of Field
- Temporal anti aliasing
- Motion blur
- Bloom
- Average exposure
- Barrel/pincushion disortion
- Chromatic dispersion
- Tonemapping and some final color adjustments
- FidelityFX RCAS final sharpening
- Lots of configurable shader options for above features
- Correct held object support for SSGI, SSAO, Screen space shadow, reflection, DoF and TAA
- Compatible with Distant Horizons, Voxy, Colorwheel and Physics Mod Pro

As a compartion to the full version, it does not use voxelization and world space ray tracing, reducing volumetric light and reflection from computing 2 times to 1 time, losing multiple bounce reflection, but have much better performance and mod compatibility.

## Known issues

- As a deferred-rendering shaders, it does not work well on mods that use transparent objects without writing to depth, and can only see the closest transparent objects, like you cannot see water behind stained glass blocks
- Due to terrain culling in shadow and render distance limit, sometimes you may see sunlight leaks in caves and buildings, this is not that resolvable on shader side
- Minecraft 26.1's rendering order is very bad, causing some overlay designed to decorate solid object are rendering with transparent obejcts, causing enchantment glint, horse marking, banner pattern, spider/enderman eyes and so on cannot rendered correctly on deferred-rendering shaders, and very expensive to resolve on shader side
- Certain versions of Optifine (like 1.21.2 to 1.21.8 J6 Pre15) cannot use vanilla light texture in deferred pipeline correctly, disable `Mod support > Mod night vision compat` can fix it on those versions

---

## 📜 许可证 / License

本项目基于 **GNU General Public License v3.0** 发布 — 详见 [LICENSE](./LICENSE)。

This project is licensed under the **GNU General Public License v3.0** — see [LICENSE](./LICENSE).

---

### 致谢 / Credits

- [GeForceLegend/Sundial-Lite](https://github.com/GeForceLegend/Sundial-Lite) — 原始光影 / Original shaderpack
- [MoAoXnX/Helian-mmco_Sundial-Lite_edit](https://github.com/MoAoXnX/Helian-mmco_Sundial-Lite_edit) — Helian 改版 / Helian edit
- [187J3X1-114514/superresolution](https://github.com/187J3X1-114514/superresolution) — Super Resolution 模组 / SR Mod
