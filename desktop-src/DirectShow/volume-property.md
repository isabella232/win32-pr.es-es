---
description: La propiedad Volume establece o recupera el volumen del altavoz para la salida de la secuencia de audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume (Propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632885"
---
# <a name="volume-property"></a>Volume (Propiedad)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `Volume` propiedad establece o recupera el volumen del altavoz para la salida de la secuencia de audio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valor devuelto

Devuelve el nivel de volumen como atenuación en decibelios como un entero.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura con un valor predeterminado de 0. El volumen completo es 0 y 10 000 es silencio. la escala es logarítmica. Multiplique el nivel de decibelio deseado por 100 (por ejemplo, 10 000 = 100 dB).

 

 



