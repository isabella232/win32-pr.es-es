---
description: El método GetVideoSize recupera las dimensiones de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Método GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677197"
---
# <a name="getvideosize-method"></a>Método GetVideoSize

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetVideoSize` método recupera las dimensiones de vídeo nativas.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto [DVDRect](dvdrect-object.md) que contiene cuatro propiedades de lectura y escritura: (superior izquierda) x; (superior izquierda) y, ancho y alto. Las propiedades **x** e **y** se establecen en cero y las otras dos propiedades reflejan el ancho y el alto del rectángulo del vídeo tal como se creó en el disco.

 

 



