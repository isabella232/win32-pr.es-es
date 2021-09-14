---
title: Método Player.close
description: El método close libera Reproductor de Windows Media recursos.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- método close Reproductor de Windows Media
- método close Reproductor de Windows Media , clase Player
- Clase de reproductor Reproductor de Windows Media método , close
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242462"
---
# <a name="playerclose-method"></a>Método Player.close

El **método close** libera Reproductor de Windows Media recursos.

## <a name="syntax"></a>Sintaxis


```JScript
Player.close()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método cierra el archivo multimedia digital actual, no Reproductor de Windows Media sí mismo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que, al hacer clic en él, detiene la reproducción en Reproductor de Windows Media y libera los recursos en uso. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





