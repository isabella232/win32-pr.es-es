---
description: La propiedad Volume establece o recupera el volumen del altavoz para la salida de la secuencia de audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume (Propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543766"
---
# <a name="volume-property"></a>Volume (Propiedad)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `Volume` propiedad establece o recupera el volumen del altavoz de la salida de la secuencia de audio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valor devuelto

Devuelve el nivel de volumen como atenuación en decibelios como un entero.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura con un valor predeterminado de 0. El volumen completo es 0 y 10.000 es el silencio; la escala es logarítmica. Multiplique el nivel de decibelios deseado por 100 (por ejemplo 10.000 = 100 dB).

 

 



