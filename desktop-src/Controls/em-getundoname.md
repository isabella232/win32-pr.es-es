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
ms.openlocfilehash: d133038c0adad2fe7eaa1ae98cf638fe6bd13fad82df3b3d2d1ac384a30e1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576645"
---
# <a name="em_getundoname-message"></a>Mensaje \_ GETUNDONAME de EM

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

## <a name="remarks"></a>Comentarios

Los tipos de acciones que se pueden deshacer o volver a escribir incluyen operaciones de escritura, eliminación, arrastrar, colocar, cortar y pegar. Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden deshacer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





