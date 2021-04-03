---
description: El evento ShowMenu se envía cuando el disco habilita o deshabilita el modo en que se muestra un menú.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997885"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowMenu` evento se envía cuando el disco habilita o deshabilita el modo en que se muestra un menú.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Especifica el menú que se ha habilitado o deshabilitado como valor numérico.



| Value | Descripción |
|-------|-------------|
| 2     | Título       |
| 3     | Root        |
| 4     | Subimagen  |
| 5     | Audio       |
| 6     | Ángulo       |
| 7     | Capítulo     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Especifica si la operación está habilitada o deshabilitada como un valor booleano.

</dd> </dl>

 

 



