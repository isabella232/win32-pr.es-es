---
description: La propiedad CursorType establece o recupera el tipo de cursor actual.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Propiedad CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdbe34f2f400c9dd291201fd4a81a032ef2cd7f16adde98df8583b6c052a4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053125"
---
# <a name="cursortype-property"></a>Propiedad CursorType

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CursorType` propiedad establece o recupera el tipo de cursor actual.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el tipo de cursor.

## <a name="remarks"></a>Comentarios

Los posibles valores para esta propiedad son:



| Value | Descripción |
|-------|-------------|
| 0     | Flecha       |
| 1     | Acercar     |
| 2     | Alejar    |
| 3     | Mano        |
| -1    | Ninguno        |



 

Esta propiedad es de lectura y escritura con un valor predeterminado de cero. Cuando se acerca la imagen, al establecer en Mano (0x3) se coloca la aplicación en modo de arrastre, lo que permite al usuario mover la imagen dentro del área de visualización `CursorType` del vídeo. 

 

 



