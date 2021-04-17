---
title: Player. enableContextMenu
description: La propiedad enableContextMenu especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Media Player de Windows Player. enableContextMenu
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
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698674"
---
# <a name="playerenablecontextmenu"></a>Player. enableContextMenu

La propiedad **enableContextMenu** especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.

## <a name="syntax"></a>Sintaxis

*reproductor*. **enableContextMenu**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un valor booleano de lectura/escritura.



| Value | Descripción                       |
|-------|-----------------------------------|
| true  | Predeterminada. Habilita el menú contextual. |
| false | No habilite el menú contextual.   |



 

## <a name="remarks"></a>Observaciones

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

**Windows Media Player 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





