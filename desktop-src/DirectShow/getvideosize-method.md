---
description: El método GetVideoSize recupera las dimensiones de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: GetVideoSize (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21746242211357e9e58e825d8e217799953dd569e91765acabe11fc2252d17c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536595"
---
# <a name="getvideosize-method"></a>GetVideoSize (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetVideoSize` método recupera las dimensiones de vídeo nativas.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un [objeto DVDRect](dvdrect-object.md) que contiene cuatro propiedades de lectura y escritura: (parte superior izquierda) x; (superior izquierda) y, Ancho y Alto. Las **propiedades x** e **y** se establecen en cero y las otras dos propiedades reflejan el ancho y el alto del rectángulo de vídeo tal y como se ha escrito en el disco.

 

 



