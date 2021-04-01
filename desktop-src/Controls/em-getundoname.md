---
title: Mensaje EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 y versiones posteriores recupera el tipo de la siguiente acción de deshacer, si existe. Microsoft Rich Edit 1,0 este mensaje no se admite.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996824"
---
# <a name="em_getundoname-message"></a>\_Mensaje GETUNDONAME em

Microsoft Rich Edit 2,0 y versiones posteriores: recupera el tipo de la siguiente acción de deshacer, si existe.

Microsoft Rich Edit 1,0: este mensaje no se admite.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si hay una acción de deshacer, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la siguiente acción en la cola de deshacer del control.

Si no hay ninguna acción que se pueda deshacer o se desconoce el tipo de la siguiente acción de deshacer, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Entre los tipos de acciones que se pueden deshacer o rehacer se incluyen las operaciones de escribir, eliminar, arrastrar, colocar, cortar y pegar. Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden deshacer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**rehacer EM \_**](em-redo.md)
</dt> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





