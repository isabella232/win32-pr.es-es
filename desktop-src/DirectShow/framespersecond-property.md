---
description: La propiedad FramesPerSecond recupera la velocidad de fotogramas de vídeo para el título actual del DVD.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propiedad FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677105"
---
# <a name="framespersecond-property"></a>Propiedad FramesPerSecond

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `FramesPerSecond` propiedad recupera la velocidad de fotogramas de vídeo del título actual del DVD.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa la velocidad de fotogramas de vídeo; 25 o 30 fotogramas por segundo.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. Las señales de vídeo NTSC se muestran en 30 fotogramas por segundo. PAL se muestra en 25 fotogramas por segundo. Un disco se codifica para reproducirse en NTSC o PAL, pero no puede reproducirse en ambos.

 

 



