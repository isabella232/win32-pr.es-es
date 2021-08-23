---
title: Uso de PlaySound para reproducir Waveform-Audio archivos
description: Uso de PlaySound para reproducir Waveform-Audio archivos
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio de forma de onda, función PlaySound
- audio de forma de onda, reproducir archivos
- audio de forma de onda, extensión de nombre de archivo WAV
- Función PlaySound, reproducir archivos de audio de forma de onda
- reproducir archivos de audio de forma de onda, función Play Sound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa83125665e2a99cc0f47da0893cbc113c0be7a251d62eb66a91e7a1218dac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687855"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Uso de PlaySound para reproducir Waveform-Audio archivos

La mayoría de los archivos de audio de forma de onda usan . Extensión de nombre de archivo WAV.

La siguiente instrucción reproduce C: \\ SOUNDS \\ BELLS. Archivo WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Si el archivo especificado no existe o si el archivo no cabe en la memoria disponible, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduce el sonido del sistema predeterminado. Si no se ha definido ningún sonido predeterminado del sistema, Se produce un error **en PlaySound** sin producir ningún sonido. Si no desea que se reprodgue el sonido del sistema predeterminado, especifique la marca SND NODEFAULT, como se \_ muestra en el ejemplo siguiente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 