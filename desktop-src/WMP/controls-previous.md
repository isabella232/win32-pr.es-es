---
title: Controls. Previous (método)
description: El método anterior establece el elemento actual en el elemento anterior de la lista de reproducción.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- método anterior de Windows Media Player
- método anterior Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método Previous
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699899"
---
# <a name="controlsprevious-method"></a>Controls. Previous (método)

El método **anterior** establece el elemento actual en el elemento anterior de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la lista de reproducción está en la primera entrada cuando se invoca el **anterior** , la última entrada de la lista de reproducción se convertirá en la actual.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que utiliza **Previous** para moverse al elemento anterior de la lista de reproducción actual. El objeto **Player** se creó con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. Next**](controls-next.md)
</dt> <dt>

[**Controls. STOP**](controls-stop.md)
</dt> </dl>

 

 





