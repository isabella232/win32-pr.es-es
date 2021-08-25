---
title: EM_GETREDONAME mensaje (Richedit.h)
description: Recupera el tipo de la acción siguiente, si la hay, en la cola de rehacer del control de edición enriquecido.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9687ae54223ec7cc0f908d747eff2504216b79469b5f285863f8c8ffdfe91b3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048825"
---
# <a name="em_getredoname-message"></a>Mensaje \_ GETREDONAME DE EM

Recupera el tipo de la acción siguiente, si la hay, en la cola de rehacer del control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la cola de rehacer del control no está vacía, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la acción siguiente en la cola de rehacer del control.

Si no hay ninguna acción que se puede rehacer o se desconoce el tipo de la siguiente acción que se puede rehacer, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Los tipos de acciones que se pueden deshacer o volver a escribir incluyen operaciones de escritura, eliminación, arrastrar y colocar, cortar y pegar. Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones rehables.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





