---
title: EM_GETUNDONAME mensaje (Richedit.h)
description: Microsoft Rich Edit 2.0 y versiones posteriores Recupera el tipo de la siguiente acción de deshacer, si la hay. Microsoft Rich Edit 1.0 Este mensaje no se admite.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062179"
---
# <a name="em_getundoname-message"></a>Mensaje \_ EM GETUNDONAME

Microsoft Rich Edit 2.0 y versiones posteriores: recupera el tipo de la siguiente acción de deshacer, si la hay.

Microsoft Rich Edit 1.0: este mensaje no se admite.

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

Si hay una acción de deshacer, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la acción siguiente en la cola de deshacer del control.

Si no hay acciones que se puedan deshacer o se desconoce el tipo de la siguiente acción de deshacer, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Entre los tipos de acciones que se pueden deshacer o reescribir se incluyen operaciones de escritura, eliminación, arrastrar, colocar, cortar y pegar. Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden deshacer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**REDO DE EM \_**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





