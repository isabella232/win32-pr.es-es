---
description: El evento ShowMenu se envía cuando el disco habilita o deshabilita la presentación de un menú.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050455"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowMenu` evento se envía cuando el disco habilita o deshabilita la presentación de un menú.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Especifica qué menú se ha habilitado o deshabilitado como un valor number.



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

 

 



