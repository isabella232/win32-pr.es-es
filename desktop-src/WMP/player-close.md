---
title: Player. Close (método)
description: El método Close libera los recursos de Media Player de Windows.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Close (método) de Windows Media Player
- Close (método) Windows Media Player, clase Player
- Clase player Windows Media Player, Close (método)
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699850"
---
# <a name="playerclose-method"></a>Player. Close (método)

El método **Close** libera los recursos de Media Player de Windows.

## <a name="syntax"></a>Sintaxis


```JScript
Player.close()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método cierra el archivo multimedia digital actual, no Media Player de Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, detiene la reproducción en Windows Media Player y libera los recursos en uso. El objeto **Player** se creó con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





