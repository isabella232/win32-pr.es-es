---
description: La propiedad FramesPerSecond recupera la velocidad de fotogramas de vídeo para el título del DVD actual.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propiedad FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061666"
---
# <a name="framespersecond-property"></a>Propiedad FramesPerSecond

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `FramesPerSecond` propiedad recupera la velocidad de fotogramas de vídeo para el título del DVD actual.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa la velocidad de fotogramas de vídeo; 25 o 30 fotogramas por segundo.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado. Las señales de vídeo ZONE se muestran a 30 fotogramas por segundo. PAL se muestra a 25 fotogramas por segundo. Un disco se codifica para reproducirse en PEM o PAL, pero no se puede reproducir en ambos.

 

 



