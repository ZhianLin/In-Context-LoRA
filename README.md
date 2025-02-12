# In-Context LoRA (IC-LoRA)

[English](./README_en.md)

🔥 **最新动态！**

- **[2024-12-17]** 🚀 我们很高兴发布 **[IDEA-Bench](https://ali-vilab.github.io/IDEA-Bench-Page/)**，这是一个旨在评估生成模型零样本任务泛化能力的综合基准。该基准包含**275**个独特案例的**100**个真实世界设计任务。尽管面向通用场景，表现最佳的模型EMU2仅获得**6.81**分（满分100），凸显了该领域当前的挑战。探索这个基准并挑战模型性能的极限吧！
- **[2024-11-16]** 🌟 社区持续创新！基于IC-LoRA的精彩项目包括**虚拟试衣、产品设计、物品迁移、角色扮演**等模型、ComfyUI节点和工作流。在**[社区创作](#community-creations-using-ic-lora)**中探索他们的作品。衷心感谢所有贡献者的卓越努力！
- **[2024-11-07]** 🚀 我们发布了**[10个预训练模型](https://huggingface.co/ali-vilab/In-Context-LoRA)**，涵盖电影分镜生成、视觉识别设计、视觉效果等多种任务。详见**[模型库](#model-zoo)**。同时提供[ComfyUI](https://github.com/comfyanonymous/ComfyUI)的[示例工作流](./workflow/film-storyboard.json)。
- **[2024-11-01]** 📂 **[In-Context LoRA](https://arxiv.org/abs/2410.23775)**的训练数据和配置已开放！
- **[2024-10-31]** 📜 最新论文**[In-Context LoRA](https://arxiv.org/abs/2410.23775)**提出了适应广泛任务的灵活框架。
- **[2024-10-19]** 🎨 发布前驱研究**[Group Diffusion Transformers](https://arxiv.org/abs/2410.15027)**，支持30个视觉生成任务的零样本学习。
- **[2024-4-18]** 💻 发布**[FlashFace](https://github.com/ali-vilab/FlashFace)**的[代码和模型](https://github.com/ali-vilab/FlashFace)，验证了注意力令牌拼接在定制生成场景中的应用。

欢迎访问**In-Context LoRA for Diffusion Transformers**的官方仓库（[论文](https://arxiv.org/abs/2410.23775) | [项目主页](https://ali-vilab.github.io/In-Context-LoRA-Page/)）。

## 社区创作

我们很高兴展示社区基于In-Context LoRA (IC-LoRA)的创新项目。如果您有推荐或想分享作品，**欢迎提交[Pull Request](https://github.com/ali-vilab/In-Context-LoRA/pulls)!**

| 项目名称 | 类型                 | 支持任务                                                                 | 示例效果 |
|--------------|----------------------|---------------------------------------------------------------------------------|----------------|
| 1. [Comfyui_Object_Migration](https://github.com/TTPlanetPig/Comfyui_Object_Migration) | ComfyUI节点 & 工作流 & LoRA模型         | 服装迁移、卡通服装转写实等     | ![示例效果](./static/386534865-9612cf8a-858d-4684-819e-7b97981d993c.png) |
| 2. [Flux Simple Try On - In Context Lora](https://civitai.com/models/950111/flux-simple-try-on-in-context-lora) | LoRA模型 & ComfyUI工作流     | 虚拟试衣             | ![示例效果](./static/example_1.png) ![示例效果](./static/ComfyUI_temp_ditfb_00016_.jpeg) |
| 3. [Flux In Context - visual identity Lora in Comfy](https://civitai.com/articles/8779) | ComfyUI工作流               | 视觉识别迁移              | ![示例效果](./static/ComfyUI_00026_.jpeg) |
| 4. [Workflows Flux In Context Lora For Product Design](https://civitai.com/models/933018/workflows-flux-in-context-lora-for-product-design) | ComfyUI工作流               | 产品设计、角色扮演等              | ![示例效果](./static/ComfyUI_temp_opjou_00016_.jpeg) |
| 5. [Flux Product Design - In Context Lora](https://civitai.com/models/933026/flux-product-design-in-context-lora) | LoRA模型 & ComfyUI工作流               | 产品设计              | ![示例效果](./static/2024-11-10-002611_0.jpeg) |
| 6. [In Context lora + Character story generator + flux+ shichen](https://civitai.com/models/951357/in-context-lora-character-story-generator-flux-shichen) | ComfyUI工作流               | 角色电影故事生成              | ![示例效果](./static/role2story.jpeg) |
| 7. [In- Context-Lora｜Cute 4koma 可爱四格漫画](https://civitai.com/models/947702/in-context-loracute-4koma) | LoRA模型 & ComfyUI工作流               | 四格漫画生成              | ![示例效果](./static/ComfyUI_00098_.jpeg) |
| 8. [Creative Effects & Design LoRA Pack (In-Context LORA)](https://civitai.com/models/929592/creative-effects-and-design-lora-pack-in-context-lora) | LoRA模型 & ComfyUI工作流               | 电影镜头生成等              | ![示例效果](./static/film-storyboard-1.jpeg) |

衷心感谢所有贡献者对IC-LoRA生态建设的杰出贡献。

## 核心思想

IC-LoRA的核心思想是将条件图像和目标图像**拼接**为复合图像，同时使用**自然语言**定义任务。这种方法能无缝适应各种应用场景。

## 功能特性

- **任务无关框架**：IC-LoRA作为通用框架，但需针对不同任务进行微调
- **定制化图像集生成**：可微调文生图模型以生成具有自定义内在关系的**图像集合**
- **基于图像集的条件生成**：支持基于一组图像生成另一组图像，实现广泛的可控生成应用

更多细节和示例请参阅[论文](https://arxiv.org/abs/2410.23775)或访问[项目主页](https://ali-vilab.github.io/In-Context-LoRA-Page/)。

## 快速开始

您可以直接使用开源的[AI-Toolkit](https://github.com/ostris/ai-toolkit)训练IC-LoRA模型。我们提供了示例训练数据和配置文件：

- **配置文件**：`config/movie-shots.yml`（放置于AI-Toolkit的`config/`目录）
- **示例数据**：`data/movie-shots.zip`（解压至AI-Toolkit的`data/movie-shots`目录）

安装依赖并配置好AI-Toolkit后，运行以下命令开始训练：

```bash
python run.py config/movie-shots.yml
```

单卡训练至少要24GB显存（可通过调整`config/movie-shots.yml`中的`resolution`参数适配不同显存），通常数小时即可完成。

## 多场景图像描述提示词

我们提供生成多场景图像描述的示例提示词：

> *为这个包含电影镜头的三场景图像创建简短描述，整个描述以[MOVIE-SHOTS]开头，后接图像整体摘要。每个场景细节应在同一句子中流畅衔接，使用[SCENE-1]、[SCENE-2]、[SCENE-3]标记各场景起始。必要时为角色赋予随机名称并用"<"和">"包裹。确保描述连贯，总字数控制在512字内。*

## 模型库

下表列出10个In-Context LoRA模型及推荐设置。我们提供[ComfyUI](https://github.com/comfyanonymous/ComfyUI)的[示例工作流](./workflow/film-storyboard.json)。

| 任务          | 模型        | 推荐设置 | 示例提示词   | 提示词翻译      |
|---------------|-------------------|---------------------|---------------------------|---------------------------|
| **1. 情侣形象设计** | [`couple-profile.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/couple-profile.safetensors)   | `宽度: 2048, 高度: 1024` | `This two-part image portrays a couple of cartoon cats in detective attire; [LEFT] a black cat in a trench coat and fedora holds a magnifying glass and peers to the right, while [RIGHT] a white cat with a bow tie and matching hat raises an eyebrow in curiosity, creating a fun, noir-inspired scene against a dimly lit background.` | `这幅两联图像描绘了身着侦探装的卡通猫情侣；[左]黑色猫咪穿着风衣戴软呢帽，手持放大镜向右凝视，[右]白色猫咪系领结戴同款帽子好奇挑眉，在昏暗背景中营造出有趣的黑色电影风格场景。` |
| **2. 电影分镜**  | [`film-storyboard.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/film-storyboard.safetensors) | `宽度: 1024, 高度: 1536`    | `[MOVIE-SHOTS] In a vibrant festival, [SCENE-1] we find <Leo>, a shy boy, standing at the edge of a bustling carnival, eyes wide with awe at the colorful rides and laughter, [SCENE-2] transitioning to him reluctantly trying a daring game, his friends cheering him on, [SCENE-3] culminating in a triumphant moment as he wins a giant stuffed bear, his face beaming with pride as he holds it up for all to see.` | `[MOVIE-SHOTS] 在热闹的节日里，[SCENE-1]害羞的男孩<Leo>站在喧嚣嘉年华边缘，瞪大眼睛惊叹于缤纷设施和欢笑声，[SCENE-2]过渡到他勉强尝试勇敢游戏的场景，朋友们为他加油，[SCENE-3]最终以他赢得巨型毛绒熊的胜利时刻收尾，他骄傲举起战利品，脸上绽放灿烂笑容。`  |
| **3. 字体设计** | [`font-design.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/font-design.safetensors)   | `宽度: 1792, 高度: 1216` | The four-panel image showcases a playful bubble font in a vibrant pop-art style. [TOP-LEFT] displays "Pop Candy" in bright pink with a polka dot background; [TOP-RIGHT] shows "Sweet Treat" in purple, surrounded by candy illustrations; [BOTTOM-LEFT] has "Yum!" in a mix of bright colors; [BOTTOM-RIGHT] shows "Delicious" against a striped background, perfect for fun, kid-friendly products. | `四联图像展示了充满活力的波普艺术风格泡泡字体。[左上]"Pop Candy"采用亮粉色波点背景；[右上]"Sweet Treat"紫色字体环绕糖果插图；[左下]"Yum!"混搭亮色；[右下]"Delicious"条纹背景，完美适合趣味儿童产品。` |
| **4. 家居装饰** | [`home-decoration.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/home-decoration.safetensors)      | `宽度: 1344, 高度: 1728` | `This four-panel image showcases a rustic living room with warm wood tones and cozy decor elements; [TOP-LEFT] features a large stone fireplace with wooden shelves filled with books and candles; [TOP-RIGHT] shows a vintage leather sofa draped in plaid blankets, complemented by a mix of textured cushions; [BOTTOM-LEFT] displays a corner with a wooden armchair beside a side table holding a steaming mug and a classic book; [BOTTOM-RIGHT] captures a cozy reading nook with a window seat, a soft fur throw, and decorative logs stacked neatly.` | `四联图像展示原木风格客厅：暖色调木材与舒适装饰；[左上]石砌壁炉搭配摆满书籍蜡烛的木架；[右上]复古皮沙发铺格子毛毯，搭配纹理靠垫；[左下]角落木椅配边桌，摆放热饮和经典书籍；[右下]窗边阅读角铺毛皮毯，整齐堆叠装饰木柴。` |
| **5. 肖像插画** | [`portrait-illustration.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/portrait-illustration.safetensors)      | `宽度: 1152, 高度: 1088` | `This two-panel image presents a transformation from a realistic portrait to a playful illustration, capturing both detail and artistic flair; [LEFT] the photograph shows a woman standing in a bustling marketplace, wearing a wide-brimmed hat, a flowing bohemian dress, and a leather crossbody bag; [RIGHT] the illustration panel exaggerates her accessories and features, with the bohemian dress depicted in vibrant patterns and bold colors, while the background is simplified into abstract market stalls, giving the scene an animated and lively feel.` | `两联图像呈现从写实肖像到趣味插画的转变；[左]照片中女士戴宽檐帽穿波西米亚裙站市场；[右]插画夸张化配饰，裙装采用鲜艳图案，背景简化为抽象摊位，营造动画般生动场景。` |
| **6. 人像摄影** | [`portrait-photography.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/portrait-photography.safetensors)      | `宽度: 1344, 高度: 1728` | `This [FOUR-PANEL] image illustrates a young artist's creative process in a bright and inspiring studio; [TOP-LEFT] she stands before a large canvas, brush in hand, adding vibrant colors to a partially completed painting, [TOP-RIGHT] she sits at a cluttered wooden table, sketching ideas in a notebook with various art supplies scattered around, [BOTTOM-LEFT] she takes a moment to step back and observe her work, adjusting her glasses thoughtfully, and [BOTTOM-RIGHT] she experiments with different textures by mixing paints directly on the palette, her focused expression showcasing her dedication to her craft.` | `[四联]图像展现年轻艺术家在明亮工作室的创作过程；[左上]执笔为大幅画布添加鲜艳色彩；[右上]坐凌乱木桌旁速写构思；[左下]退后扶镜观察作品；[右下]调色板实验不同肌理，专注神情彰显匠心。` |
| **7. PPT模板** | [`ppt-templates.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/ppt-templates.safetensors)      | `宽度: 1984, 高度: 1152` | `This four-panel image showcases a rustic-themed PowerPoint template for a culinary workshop; [TOP-LEFT] introduces "Farm to Table Cooking" in warm, earthy tones; [TOP-RIGHT] organizes workshop sections like "Ingredients," "Preparation," and "Serving"; [BOTTOM-LEFT] displays ingredient lists for seasonal produce; [BOTTOM-RIGHT] includes chef profiles with short bios.` | `四联图像展示烹饪工作坊的田园风PPT模板；[左上]"从农场到餐桌"采用大地色；[右上]组织"食材"、"准备"、"摆盘"板块；[左下]列出时令食材；[右下]包含厨师简介。` |
| **8. 沙尘暴特效** | [`sandstorm-visual-effect.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/sandstorm-visual-effect.safetensors)      | `宽度: 1408, 高度: 1600` | `[SANDSTORM-PSA] This two-part image showcases the transformation of a cyclist through a sandstorm visual effect; [TOP] the upper panel features a cyclist in vibrant gear pedaling steadily on a clear, open road with a serene sky in the background, highlighting focus and determination, [BOTTOM] the lower panel transforms the scene as the cyclist becomes enveloped in a fierce sandstorm, with sand particles swirling intensely around the bike and rider against a stormy, darkened backdrop, emphasizing chaos and power.` | `[沙尘暴公益广告]两联图像展示骑行者特效转变；[上]骑行者鲜艳装备在晴朗道路骑行；[下]沙尘暴特效笼罩骑行者，沙粒在暴风云背景下剧烈旋转，强调混乱与力量。` |
| **9. 烟花特效** | [`sparklers-visual-effect.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/sparklers-visual-effect.safetensors)      | `宽度: 960, 高度: 1088` | [REAL-SPARKLERS-OVERLAYS] The two-part image vividly illustrates a woodland proposal transformed by sparkler overlays; [TOP] the first panel depicts a man kneeling on one knee with an engagement ring before his partner in a forest clearing at dusk, with warm, natural lighting, [BOTTOM] while the second panel introduces glowing sparklers that form a heart shape around the couple, amplifying the romance and joy of the moment. | `[真实烟花叠加]两联图像展现森林求婚场景转换；[上]黄昏林间男子单膝跪地求婚；[下]烟花构成心形环绕情侣，增强浪漫氛围。` |
| **10. 视觉识别设计** | [`visual-identity-design.safetensors`](https://huggingface.co/ali-vilab/In-Context-LoRA/blob/main/visual-identity-design.safetensors)      | `宽度: 1472, 高度: 1024` | `The two-panel image showcases the joyful identity of a produce brand, with the left panel showing a smiling pineapple graphic and the brand name “Fresh Tropic” in a fun, casual font on a light aqua background; [LEFT] while the right panel translates the design onto a reusable shopping tote with the pineapple logo in black, held by a person in a market setting, emphasizing the brand’s approachable and eco-friendly vibe.` | `两联图像展示农产品品牌视觉识别；[左]浅蓝背景微笑菠萝图案与"Fresh Tropic"趣味字体；[右]黑色菠萝logo帆布袋在市场场景中的应用，突出品牌亲和力与环保理念。` |

## 许可证

本仓库使用[FLUX](https://github.com/black-forest-labs/flux)作为基础模型，使用时需遵守FLUX的[许可证](https://github.com/black-forest-labs/flux/tree/main/model_licenses)。

**免责声明**：本仓库提供的训练数据可能包含受版权保护的内容，开源数据仅供研究参考。如需商用，请自行获取相关授权并确保符合版权法规。

## 引用

如果您的研究中使用本工作，请引用：

```bibtex
@article{lhhuang2024iclora,
  title={In-Context LoRA for Diffusion Transformers},
  author={Huang, Lianghua and Wang, Wei and Wu, Zhi-Fan and Shi, Yupeng and Dou, Huanzhang and Liang, Chen and Feng, Yutong and Liu, Yu and Zhou, Jingren},
  journal={arXiv preprint arxiv:2410.23775},
  year={2024}
}
```

```bibtex
@article{lhhuang2024groupdiffusion,
  title={Group Diffusion Transformers are Unsupervised Multitask Learners},
  author={Huang, Lianghua and Wang, Wei and Wu, Zhi-Fan and Dou, Huanzhang and Shi, Yupeng and Feng, Yutong and Liang, Chen and Liu, Yu and Zhou, Jingren},
  journal={arXiv preprint arxiv:2410.15027},
  year={2024}
}
```