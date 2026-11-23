# Changelog

All notable changes to ZYpsilon. Dates are release dates. · [Italiano](#italiano) · [中文](#中文)

## 1.2.3 — 2026-11-23

### Added
- **Search engines and AI assistants**: Italian, English and Chinese landing pages (`/it/`, `/en/`, `/zh/`), `sitemap.xml`, `robots.txt`, `llms.txt`, language alternates (hreflang) and structured data (JSON-LD) on the home page.

### Changed
- **The app now opens on orthogonal projections, "Faces parallel to the planes"** (it used to open on accidental perspective). Links and scenes saved earlier open exactly as before.
- **Cutting plane**: when switched on it appears tilted 30° to the horizontal plane, perpendicular to the vertical plane and rising from left to right as seen from the picture plane. In the free cutting plane (axonometry, perspective) rotation 0° now means exactly this position; scenes saved before 1.2.3 are converted automatically.
- **Horizontal picture plane**: the cutting plane now ends just above the solid instead of extending far beyond it; the black ground line is drawn on the lower edge of the picture plane.
- **Horizontal picture plane**: in the oblique axonometries where the picture plane lies on the horizontal plane (planometric, lowered planometric, military) the horizontal plane (floor and grid) coincides with the picture plane and is no longer drawn; the *Horizontal plane* checkbox is hidden in these views.

## 1.2.2 — 2026-11-23

### Added
- **Drawing sheet** in every mode (ZYpsilon and Intersection Lab). The *Sheet* button chooses A4, A3 or A2, landscape or portrait. All measures (sliders, readouts, distances from the planes) are in **centimetres** and the drawing is 1:1. Orthogonal projections: the sheet is divided in four by the ground line and the LP axis — VP top left, LP top right, HP bottom left (PV · PL · PO in Italian, VP · LP · HP in English, 正立面 · 侧立面 · 水平面 in Chinese); folding the planes shows the sheet with its border (20 mm binding margin on the left, 10 mm elsewhere) in space. Axonometry and perspective: the picture plane is the sheet; in perspective it also shows the ground line, the horizon line, the principal point, the observer's point of view folded onto the horizon and the vanishing points (the distance points for a frontal perspective). In the 3D view the folded projection planes keep their colour; the drawing board (border, axes, plane abbreviations, format) lives only in the sheet space.
- **Lay out** button, next to the sheet-format button. In perspective it centres the whole construction (figure, ground line, horizon, folded station point, vanishing points) without moving the solid; in the other modes it positions the solid so that each view sits in the middle of its quadrant (orthogonal projections) or the image in the middle of the border.
- **Sheet advice instead of automatic scaling**: the drawing is never rescaled automatically. A short notice appears only when something does not fit the border — the solid views (it says how much the measures would have to be reduced, e.g. 1:2 or halved, or which larger sheet would do), the construction lines (folding, horizon, vanishing points, station point), or the drawing is simply not centred (use *Lay out*) — and disappears as soon as everything is inside. It is not printed in PNG/PDF.
- **Measure limits calibrated on A3** (hexagonal prism, side = height, as reference): orthogonal projections 2–15 cm, axonometry 3–14 cm, perspective 5–30 cm.
- **Fixed bottom-centre bar**, always centred (it only moves to the left on very narrow windows): layouts, **Download** (*Image (PNG)* or *PDF*) and **Link**, which moved there from the top right.
- **PDF export**: the page is the chosen sheet format (A3 landscape if none); the ZYpsilon mark and website sit inside the border, bottom right, and are a clickable link that reopens the very drawing in the PDF (same scene, language, sheet format and layout). Scenes (links and Save/Open) now also keep the selected sheet. The PNG carries the same mark.
- **Click a vertex** (orthogonal projections, in ZYpsilon and in the Lab), in space or on its PV/PO/PL images: a card shows its exact distances from the three projection planes in cm and lets you type new values — the solid moves accordingly (in the Lab, the solid the vertex belongs to, or both for points of the intersection curve).
- **Intersection Lab — generatrices**: points of the curve that fall on a face of a solid and not on an edge get their **generic line**, drawn thin, dashed and green (on a pyramid from the apex through the point to the base perimeter, on a prism parallel to the axis from base to base), in the three views, in the 3D view and on the sheet; it follows the *Construction lines* option.
- Touch screens and interactive whiteboards work: one finger rotates, two fingers pan and zoom (already the case; now documented).

### Changed
- **Start language**: the application opens in the browser language — Italian, Chinese, or English for any other language. A language chosen with the selector is remembered; `?lang=it|en|zh` force one (this replaces the 1.2.1 behaviour, always English).
- **Nomenclature of points, checked against textbooks in the three languages**: Italian — every point is a capital letter: space points A, projections A′ (PO), A″ (PV), A‴ (PL), rabatted point (A), images on the picture plane A\*, A\*′, A\*₀ (lower case stays for lines, Greek letters for planes); English and Chinese (GB convention) — space points in capitals, projections in lower case a (H), a′ (V), a″ (W). In Chinese the points are Latin letters A, B, C … (the characters 甲乙丙 are no longer used for points).
- **Line hierarchy on the drawing sheet** (Lab sheet, its 3D view and the standard sheet): construction lines (projectors, arcs, generatrices) are thin, light and continuous; projection outlines are darker and heavier; hidden edges stay dark and dashed.
- **Intersection Lab — centring**: the centre of a solid is the point at half its height on the axis through the centre of its base figure, so a solid no longer shifts when it is rotated about its axis. *Centre the two solids* makes the two centres coincide at the centre of the projection planes.
- **Intersection Lab — starting scene**: a square prism with a horizontal axis (parallel to the ground line, turned 45°) and a vertical hexagonal prism, centres coincident.
- **Intersection Lab — letters**: same format as the standard app (monospace 600, crimson with white halo, small dot, letter next to its point on the outer side of the figure); the same colours and size in the 3D view (space points dark, projections crimson). One yellow and one blue for solids A and B on every control of the left column; the *Centre* button is neutral.
- **Sections of composite solids (the ZYpsilon logo solid)**: when the section is folded onto the projection plane, every sectioned piece is shown in true shape, not only the first one; no letters are drawn on it.
- **Cookie notice**: after *Decline* the application keeps working and a short notice confirms that statistics are off, with a link to change the choice. Without consent no Analytics script is loaded and no request is sent (verified: first visit, decline, accept then decline).
- **Texts**: README (English, Italian, Chinese), the *Licences, use and privacy* page, the page description and the Zenodo/GitHub metadata describe the drawing sheet, PDF export and Intersection Lab.

### Fixed
- **Intersection Lab colours**: in some positions (including the default scene) the visible pieces of a face were computed twice, so the colours of the two solids overlapped and flickered in the images on the projection planes; coplanar faces of the two solids also flickered in the 3D view. Visible pieces are now computed without duplicates and never overlap; on coplanar faces the first solid wins and the two solids are drawn as separate meshes.
- *Lay out* in axonometry and perspective now centres vertically on the border (a unit slip had shifted the figure).

## 1.2.1 — 2026-11-22

### Changed
- The application always opens in English (the browser language is no longer used); `?lang=it` and `?lang=zh` open it in Italian or Chinese.
- The image panel starts collapsed; the starting solid is the cube, and the Intersection Lab starts with a cube (A) and a hexagonal prism (B).
- Chinese interface: points are named 甲, 乙, 丙 … (then 子, 丑 … ) in every projection, in the drawing sheet and in the Intersection Lab; projections are written 甲′ (HP), 甲″ (VP), 甲‴ (LP). The projection planes are named 正立面, 水平面, 侧立面 instead of V, H, W; no Latin "OX" on the ground line.

## 1.2.0 — 2026-11-22

### Added
- **Intersection Lab**: a teaching mode for the interpenetration of two solids by the cutting-plane method. Two solids (A, B) with their own axis, rotation and position; a cutting plane parallel to HP, VP or LP that can be animated; red dots at the crossings of the two section outlines, a node trail, and the curve of interpenetration built point by point in orthogonal projections and axonometry, with lettered points. Sliders accept typed values; *Centre the two solids*; *Colour* mode; the horizontal plane can be hidden.
- **Vanishing line of the light rays** (dashed) through FL and FL′ in the perspective shadow construction.
- Chinese interface for the lab (toggle "相贯实验室", logo tag "实验室"); full English, Italian and Chinese strings for every new control.
- `README.zh.md` (Chinese) and this changelog.

### Changed
- Shadow construction shows only the light rays through the vertices that bound the shadow outline, not every edge.
- Language review of English, Italian and Chinese: terminology, spelling and punctuation, and per-language notation of letters (points, planes, traces).
- In the Intersection Lab, letters that touch are moved apart automatically (a small, bounded shift) and drawn slightly smaller, so every point stays readable.
- `index.html` falls back to `vendor/three.min.js` when cdnjs cannot be reached, so the page also works offline.
- README rewritten in English first, with Italian and Chinese versions; Zenodo and GitHub metadata in English.

## 1.0.0 — 2026-11-20
First public release: Monge projections, orthogonal and oblique axonometry, perspective, shadows, sections, measures, save/open and shareable links, interface in three languages, PolyForm Noncommercial 1.0.0.

---

## Italiano
**1.2.3** — L'app si apre sulle proiezioni ortogonali «facce parallele ai piani» (i link e le scene salvate si aprono come prima); **piano di taglio**: compare inclinato di 30° rispetto a PO, ortogonale a PV e crescente da sinistra a destra (nel piano libero, rotazione 0° = questa posizione; le scene salvate prima vengono convertite), e nelle assonometrie con quadro orizzontale termina appena sopra il solido; **quadro orizzontale** (planometrica, planometrica ribassata, militare): il piano orizzontale coincide con il quadro e non viene disegnato, la linea di terra è sul bordo basso del quadro; pagine di presentazione in italiano, inglese e cinese, sitemap, `llms.txt` e dati strutturati per i motori di ricerca.

**1.2.2** — Nuovo **foglio da disegno** in tutte le modalità (tasto *Foglio*: A4, A3 o A2, orizzontale o verticale; misure in centimetri, disegno in scala 1:1, squadratura visibile quando si ribaltano i piani), con **Impagina** accanto al formato; il disegno non viene mai ridotto o ingrandito in automatico: un breve avviso compare solo se qualcosa non entra e scompare quando è tutto dentro; limiti delle misure tarati su A3. Barra fissa al centro in basso con **Scarica** (PNG o **PDF** nel formato del foglio, con marchio e sito cliccabili che riaprono proprio quel disegno) e **Link**; le scene conservano il foglio. Clic su un vertice per leggerne e modificarne le distanze da PV, PO e PL. Nel laboratorio: centro del solido a metà altezza sull'asse della base, *Centra* fa coincidere i due centri, scena iniziale con prisma a base quadrata (asse orizzontale) e prisma esagonale verticale, retta generica per i punti sulle facce, un solo giallo e un solo azzurro, **colori dei due solidi corretti** (niente più sovrapposizioni e sfarfallii nelle immagini sui piani e nella vista 3D). Nomenclatura verificata nelle tre lingue (it: A, A′ PO, A″ PV, A‴ PL, (A) ribaltato; en e zh: A nello spazio, a, a′, a″ nelle proiezioni; in cinese i punti sono lettere latine); lingua iniziale = lingua del browser; dopo il rifiuto del consenso l'app resta utilizzabile; sezione dei solidi composti con tutti i pezzi in vera forma; linee di richiamo sottili e chiare, contorni più marcati; testi (README, pagina Licenze/uso/privacy, descrizione) aggiornati.

**1.2.1** — Avvio sempre in inglese, riquadro dell'immagine chiuso, cubo come solido iniziale (anche nel lab, con A cubo e B prisma esagonale); in cinese punti e piani senza lettere latine (甲乙丙…, 正立面/水平面/侧立面).

**1.2.0** — Nuovo *Laboratorio di compenetrazione* (due solidi, piano secante scorrevole e animabile, punti della curva in Monge e assonometria); *retta di fuga dei raggi luminosi* tratteggiata; nelle ombre si disegnano solo i raggi dei vertici che delimitano il contorno; lettere del lab che si toccano si spostano da sole e sono un po' più piccole; revisione linguistica in italiano, inglese e cinese; funzionamento offline di `index.html`; README in inglese, italiano e cinese.

## 中文
**1.2.3** — 应用默认以正投影“各面平行于投影面”打开（旧链接和已保存的场景照常打开）；**截平面**：开启时与水平投影面成30°、垂直于正立面并自左向右升高（自由平面中旋转0°即此位置，旧场景自动转换），在画面水平的轴测图中止于立体上方；**水平画面**（平面轴测、降低平面轴测、军事轴测）：水平面与画面重合，不再绘制，地平线位于画面下缘；新增意大利语、英语和中文介绍页、站点地图、`llms.txt` 和结构化数据，便于搜索引擎收录。

**1.2.2** — 新增**图纸**，适用于所有模式（“图纸”按钮：A4、A3 或 A2，横向或纵向；尺寸以厘米计，图样按 1:1；折倒投影面时显示图框），并在幅面按钮旁增加**排版**；图样绝不会自动缩放：只有放不下时才出现简短提示，全部落入图框后即消失；尺寸范围按 A3 标定。底部居中的固定工具条含**下载**（PNG 或按图纸幅面的 **PDF**，其中的标志和网址可点击并重新打开该幅图）和**链接**；场景会保留所选图纸。点击顶点可读取并修改它到 PV、PO、PL 的距离。实验室：立体的中心位于底面轴线的半高处，*居中*使两个中心重合，初始场景为轴线水平的正四棱柱与竖直的正六棱柱，相贯线上落在表面的点带有母线，立体甲/乙各用统一的黄色与蓝色，并**修正了两个立体的颜色**（投影面图像和三维视图中不再重叠、闪烁）。三种语言的符号规范已核对（意大利语：A、A′ 水平、A″ 正立、A‴ 侧立、(A) 折倒；英语和中文：空间点用大写，投影用 a、a′、a″；中文的点使用拉丁字母）；初始语言跟随浏览器；拒绝同意后应用仍可使用；复合立体的剖切显示所有截断块的实形；作图线更细更浅，轮廓线更粗；文本（README、许可/使用/隐私页面、页面描述）已更新。

**1.2.1** — 应用始终以英语打开；图像小窗默认收起；初始立体为立方体（相贯实验室中立体甲为立方体、立体乙为六棱柱）；中文界面中的点和投影面不再使用拉丁字母（甲乙丙……，正立面/水平面/侧立面）。

**1.2.0** — 新增**相贯实验室**（两个立体、可滑动并可动画的截平面、在正投影和轴测图中逐点生成相贯线）；虚线的**光线灭线**；阴影作图只绘出构成阴影轮廓的顶点所引的光线；相贯实验室中相互重叠的字母会自动错开并略微缩小；对英、意、中三种语言做了语言审校；`index.html` 可离线运行；提供英、意、中三种 README。
