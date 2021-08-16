---
description: La propiedad SubpictureStreamsAvailable recupera el número de secuencias de subimagen disponibles en el título actual.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propiedad SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2349cb696c1f6d363fefb6a6e90a662fa7c3233b3b0aefcb57d381a604f41832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633445"
---
# <a name="subpicturestreamsavailable-property"></a>Propiedad SubpictureStreamsAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `SubpictureStreamsAvailable` propiedad recupera el número de secuencias de subimagen disponibles en el título actual.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve el número de secuencias disponibles como un entero.

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. Para consultar su atributo de lenguaje en cada secuencia, primero llame a este método para obtener el límite superior.

La numeración de secuencias es de base cero.

 

 



