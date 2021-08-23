---
title: Player.enableContextMenu
description: La propiedad enableContextMenu especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic con el botón derecho del mouse.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player.enableContextMenu Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ead93634131483ab1a79c396453f7fa5918c8c5f82eae8bf253a70e74a6d7f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836226"
---
# <a name="playerenablecontextmenu"></a>Player.enableContextMenu

La **propiedad enableContextMenu** especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic con el botón derecho del mouse.

## <a name="syntax"></a>Syntax

*player*. **enableContextMenu**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura y escritura.



| Valor | Descripción                       |
|-------|-----------------------------------|
| true  | Predeterminada. Habilite el menú contextual. |
| false | No habilite el menú contextual.   |



 

## <a name="remarks"></a>Comentarios

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





