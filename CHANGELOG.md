# Changelog

All notable changes to ZYpsilon. Dates are release dates. · [Italiano](#italiano) · [中文](#中文)

## 1.2.0 — 2026-11-22

### Added
- **Intersection Lab**: a teaching mode for the interpenetration of two solids by the cutting-plane method. Two solids (A, B) with their own axis, rotation and position; a cutting plane parallel to HP, VP or LP that can be animated; red dots at the crossings of the two section outlines, a node trail, and the curve of interpenetration built point by point in orthogonal projections and axonometry, with lettered points. Sliders accept typed values; *Centre the two solids*; *Colour* mode; the horizontal plane can be hidden.
- **Vanishing line of the light rays** (dashed) through FL and FL′ in the perspective shadow construction.
- Chinese interface for the lab (toggle "相贯实验室", logo tag "实验室"); full English, Italian and Chinese strings for every new control.
- `README.zh.md` (Chinese) and this changelog.

### Changed
- Shadow construction shows only the light rays through the vertices that bound the shadow outline, not every edge.
- Language review of English, Italian and Chinese: terminology, spelling and punctuation, and per-language notation of letters (points, planes, traces).
- `index.html` falls back to `vendor/three.min.js` when cdnjs cannot be reached, so the page also works offline.
- README rewritten in English first, with Italian and Chinese versions; Zenodo and GitHub metadata in English.

## 1.0.0 — 2026-11-20
First public release: Monge projections, orthogonal and oblique axonometry, perspective, shadows, sections, measures, save/open and shareable links, interface in three languages, PolyForm Noncommercial 1.0.0.

---

## Italiano
**1.2.0** — Nuovo *Laboratorio di compenetrazione* (due solidi, piano secante scorrevole e animabile, punti della curva in Monge e assonometria); *retta di fuga dei raggi luminosi* tratteggiata; nelle ombre si disegnano solo i raggi dei vertici che delimitano il contorno; revisione linguistica in italiano, inglese e cinese; funzionamento offline di `index.html`; README in inglese, italiano e cinese.

## 中文
**1.2.0** — 新增**相贯实验室**（两个立体、可滑动并可动画的截平面、在正投影和轴测图中逐点生成相贯线）；虚线的**光线灭线**；阴影作图只绘出构成阴影轮廓的顶点所引的光线；对英、意、中三种语言做了语言审校；`index.html` 可离线运行；提供英、意、中三种 README。
