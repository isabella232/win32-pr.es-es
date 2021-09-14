---
title: Uso de Play Sound para reproducir Waveform-Audio archivos
description: Uso de Play Sound para reproducir Waveform-Audio archivos
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio de forma de onda, función Play Sound
- audio de forma de onda, reproducir archivos
- audio de onda, extensión de nombre de archivo WAV
- Función Play Sound, reproducir archivos de audio de forma de onda
- reproducir archivos de audio de forma de onda, función Play Sound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071742"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Uso de Play Sound para reproducir Waveform-Audio archivos

La mayoría de los archivos de audio de forma de onda usan . Extensión de nombre de archivo WAV.

La siguiente instrucción reproduce la C: \\ SOUNDS \\ BELLS. Archivo WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Si el archivo especificado no existe o si el archivo no cabe en la memoria disponible, [**Play Sound**](/previous-versions//dd743680(v=vs.85)) reproduce el sonido predeterminado del sistema. Si no se ha definido ningún sonido predeterminado del sistema, **Play Sound** produce un error sin producir ningún sonido. Si no desea que se reprodgue el sonido del sistema predeterminado, especifique la marca SND NODEFAULT, como se \_ muestra en el ejemplo siguiente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 