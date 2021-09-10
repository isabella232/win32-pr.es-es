---
title: Uso de Play Sound para sonidos de bucle
description: Uso de Play Sound para sonidos de bucle
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- audio de forma de onda, función Play Sound
- audio de forma de onda, sonidos de bucle
- audio de onda, parámetro fdw Sound
- Función Play Sound, sonidos de bucle
- Función Play Sound, parámetro fdw Sound
- bucles de sonidos de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372488"
---
# <a name="using-playsound-to-loop-sounds"></a>Uso de Play Sound para sonidos de bucle

Si especifica las marcas SND LOOP y SND ASYNC para el parámetro fdw Sound de la función Play Sound, el sonido se seguirá reproyendo repetidamente, como se muestra en el \_ \_ ejemplo siguiente:  [](/previous-versions//dd743680(v=vs.85))


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Si desea crear un bucle de un sonido, debe reproducirlo de forma asincrónica; no puede usar la marca SND \_ SYNC con la marca SND \_ LOOP. Un sonido en bucle seguirá reproyéndolo hasta que llame a **Play Sound** para reproducir otro sonido. Para detener la reproducción de un sonido (en bucle o asincrónico) sin reproducir otro sonido, use la instrucción siguiente:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 