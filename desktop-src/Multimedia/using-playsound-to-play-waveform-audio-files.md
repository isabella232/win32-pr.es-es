---
title: Usar PlaySound para reproducir archivos de Waveform-Audio
description: Usar PlaySound para reproducir archivos de Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio de onda, función PlaySound
- audio de onda, reproducir archivos
- audio de onda, extensión de nombre de archivo WAV
- Función PlaySound, reproducir archivos de audio de onda
- reproducir la onda-archivos de audio, función PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995248"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Usar PlaySound para reproducir archivos de Waveform-Audio

La mayoría de los archivos de audio de onda usan. Extensión de nombre de archivo WAV.

La siguiente instrucción reproduce las \\ campanas C: Sounds \\ . Archivo WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Si el archivo especificado no existe, o si el archivo no cabe en la memoria disponible, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduce el sonido predeterminado del sistema. Si no se ha definido ningún sonido del sistema predeterminado, se produce un error en **PlaySound** sin generar ningún sonido. Si no desea que se reproduzca el sonido del sistema predeterminado, especifique la \_ marca SND nodefault, tal como se muestra en el ejemplo siguiente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 