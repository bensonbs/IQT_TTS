# IQT_TTS

目前，我正在評估 VALL-E X 和 XTTS 兩種語音合成技術：

- VALL-E X 在重現真實語氣和音色方面表現出色，但其生成過程目前還不夠穩定。
  
- XTTS 經過微調能夠模擬出台灣口音，且其語音生成過程相對更為穩定。

另外，值得注意的是：
  - VALL-E X 在使用音頻提示（Audio Prompt）進行生成時會出現穩定性問題，因此我沒有提供包含音頻提示的生成音檔。
  - VALL-E X 的基礎模型（Base model）在不使用音頻提示的情況下會隨機生成不同角色的聲音，故也沒有附上基礎模型的生成音檔示例。

## Case 1
```
生成文字: 這裡是網際智慧的'語音生成'服務, 我是xx，現在是人工智能生成的語音
```

VALL-E X finetune 4 hr (生成5~10次挑選最佳)
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
|  vallex-ft   |      -       |[vallex-base-demo01-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/73150a10-3a3e-4608-aa00-d48e2e0d3980)|



XTTS-base
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep3  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)|[xtts-base-demo01-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/0187df9c-e577-44ab-9d97-95c6635af18e)
| xtts-ft-ep3  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)|[xtts-base-demo01-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/18f2d4dd-612a-4eac-8cf9-abdc2634cc5d)
| xtts-ft-ep3  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)|[xtts-base-demo01-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/b7f7ca91-c747-4e6b-9fa8-5fdfaa52dc2e)



XTTS-finetune 3 Epoch
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep3  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)| [xtts-ft-ep3-demo01-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/78306644-78dc-431f-9656-6701cc46aca7)|
| xtts-ft-ep3  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)| [xtts-ft-ep3-demo01-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/5fa7f64f-130e-4c31-9afc-046d8d869b76)|
| xtts-ft-ep3  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)| [xtts-ft-ep3-demo01-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/98bbe871-fb11-428d-bf8f-132051faace7)

XTTS-finetune 19 Epoch
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep19  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)| [xtts-ft-ep19-demo01-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/fc9363ae-ae81-448d-90ad-6d1c66413dd2)
| xtts-ft-ep19  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)| [xtts-ft-ep19-demo01-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/34dc3830-d5ac-4cf9-8b9c-f6f9b661a848)
| xtts-ft-ep19  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)|[xtts-ft-ep19-demo01-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/a0eae694-5b2c-4796-9f63-770a0fa94324)


## Case 2
```
生成文字: 現代的女性真的要成為一個,靠自己的勞力經濟獨立的女性嗎? 我們在他的小說裡會看到許許多多這樣的一個心情的女性描繪.
```

VALL-E X finetune 4 hr (生成5~10次挑選最佳)
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
|  vallex-ft   |      -       |[vallex-base-demo02-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/b918bc29-1bc4-482d-8591-be07b757cba2)|


XTTS-base
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep3  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)|[xtts-base-demo02-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/27f0083e-7e8f-4b2f-97f4-b5438b1ca2dc)
| xtts-ft-ep3  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)|[xtts-base-demo02-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4a268411-1945-4dc8-864a-631195282935)
| xtts-ft-ep3  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)|[xtts-base-demo02-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/bcf0049a-2731-45dc-a296-596a6dcab6f3)

XTTS-finetune 3 Epoch
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep3  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)| [xtts-ft-ep3-demo02-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/73c83e27-5ab3-4429-b8d1-cfde336079b0)
| xtts-ft-ep3  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)| [xtts-ft-ep3-demo02-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/5a579d93-331a-4d3d-97dd-6fea9fbab5c0)
| xtts-ft-ep3  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)| [xtts-ft-ep3-demo02-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/bc833fc1-b0f6-4e84-8274-d285a3e89a94)

XTTS-finetune 19 Epoch
| Model        | Audio Prompt | Generate Audio |   
|--------------|--------------|----------------|
| xtts-ft-ep19  |[dr-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/047ba0f5-05a1-4e04-9cda-87e812888c1f)| [xtts-ft-ep19-demo02-dr.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/d2a72354-2aaa-4093-b938-443110f1a1f5)
| xtts-ft-ep19  |[js-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/f33d1414-9ce1-40fa-bdcd-ce5e2cc6b375)| [xtts-ft-ep19-demo02-js.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/c737be07-c742-48c8-a623-73bf340ce39f)
| xtts-ft-ep19  |[xs-1-cut.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/4622777e-708c-4cd7-b6d3-5c742a062769)| [xtts-ft-ep19-demo02-xs.webm](https://github.com/bensonbs/IQT_TTS/assets/120996184/7812ef7b-4889-465e-b0f1-b5f4dc1803f0)
