---
title: Usar PlaySound para reproducir sonidos
description: Usar PlaySound para reproducir sonidos
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- audio de onda, función PlaySound
- audio de una onda, sonidos en bucle
- audio de la onda, parámetro fdwSound
- Función PlaySound, sonidos en bucle
- Función PlaySound, parámetro fdwSound
- 'onda de onda de bucle: sonidos de audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420541"
---
# <a name="using-playsound-to-loop-sounds"></a>Usar PlaySound para reproducir sonidos

Si especifica las marcas SND \_ Loop y SND \_ Async Flags para el parámetro *fdwSound* de la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , el sonido se seguirá reproduciendo repetidamente, tal como se muestra en el ejemplo siguiente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Si desea crear un bucle de sonido, debe reproducirlo de forma asincrónica. no se puede usar la \_ marca de sincronización SND con la \_ marca de bucle SND. Un sonido en bucle continuará reproduciéndose hasta que llame a **PlaySound** para reproducir otro sonido. Para detener la reproducción de un sonido (en bucle o asincrónico) sin reproducir otro sonido, use la siguiente instrucción:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 