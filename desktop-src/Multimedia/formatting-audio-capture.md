---
title: Aplicar formato a la captura de audio
description: Aplicar formato a la captura de audio
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- CapSetAudioFormat macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36acf1f98bcb6ea5d6786264406c28da78e909e3e57c5d796eac080139229f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496385"
---
# <a name="formatting-audio-capture"></a>Aplicar formato a la captura de audio

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

 

 




