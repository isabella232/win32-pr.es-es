---
title: Aplicación de formato a la captura de audio
description: Aplicación de formato a la captura de audio
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- CapSetAudioFormat (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f53553804aab401a9c2a4ada5dc9ee39170269
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371372"
---
# <a name="formatting-audio-capture"></a>Aplicación de formato a la captura de audio

En el ejemplo siguiente se [**usa capSetAudioFormat para**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) establecer el formato de audio en PCM de 8 bits y estéreo de 11 kHz.


```C++
WAVEFORMATEX wfex;

wfex.wFormatTag = WAVE_FORMAT_PCM;
wfex.nChannels = 2;                // Use stereo
wfex.nSamplesPerSec = 11025;
wfex.nAvgBytesPerSec = 22050;
wfex.nBlockAlign = 2;
wfex.wBitsPerSample = 8;
wfex.cbSize = 0;

capSetAudioFormat(hWndC, &wfex, sizeof(WAVEFORMATEX)); 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




