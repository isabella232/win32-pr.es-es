---
description: La propiedad CursorType establece o recupera el tipo de cursor actual.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Propiedad CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906636"
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

## <a name="remarks"></a>Observaciones

Los posibles valores para esta propiedad son:



| Value | Descripción |
|-------|-------------|
| 0     | Flecha       |
| 1     | Acercar     |
| 2     | Alejar    |
| 3     | Casilla        |
| -1    | None        |



 

Esta propiedad es de lectura/escritura y su valor predeterminado es cero. Cuando se amplía la imagen, si se establece `CursorType` en **Hand** (0X3), la aplicación se coloca en modo de arrastre, lo que permite al usuario desplace la imagen dentro del área de presentación del vídeo.

 

 



