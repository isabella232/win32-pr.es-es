---
title: Uso de Sonidos de reproducción para bucles
description: Uso de Sonidos de reproducción para bucles
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- audio de forma de onda, función PlaySound
- audio de forma de onda, sonidos de bucle
- audio de forma de onda, parámetro fdwSound
- Función PlaySound, bucle de sonidos
- Función PlaySound, parámetro fdwSound
- bucles de sonidos de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf97321a72ab566bf622e725700dbf336ddba6d92b9b8e6df9150357492656f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136123"
---
# <a name="using-playsound-to-loop-sounds"></a>Uso de Sonidos de reproducción para bucles

Si especifica las marcas SND LOOP y SND ASYNC para el parámetro fdwSound de la función \_ \_ [**PlaySound,**](/previous-versions//dd743680(v=vs.85))  el sonido seguirá reprodiendo repetidamente, como se muestra en el ejemplo siguiente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Si desea hacer un bucle de un sonido, debe reproducirlo de forma asincrónica; no puede usar la marca SND \_ SYNC con la marca SND \_ LOOP. Un sonido en bucle se seguirá reproducendo hasta que llame a **PlaySound** para reproducir otro sonido. Para detener la reproducción de un sonido (en bucle o asincrónico) sin reproducir otro sonido, use la siguiente instrucción:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 