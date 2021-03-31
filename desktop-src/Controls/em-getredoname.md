---
title: Mensaje EM_GETREDONAME (RichEdit. h)
description: Recupera el tipo de la siguiente acción, si existe, en la cola de rehacer del control Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME controles de mensajes de Windows
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
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996504"
---
# <a name="em_getredoname-message"></a>\_Mensaje GETREDONAME em

Recupera el tipo de la siguiente acción, si existe, en la cola de rehacer del control Rich Edit.

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

Si la cola rehecha del control no está vacía, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la siguiente acción en la cola de puesta al día del control.

Si no hay ninguna acción que se puedan rehacer o se desconoce el tipo de la siguiente acción que se pueden rehacer, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Entre los tipos de acciones que se pueden deshacer o rehacer se incluyen las operaciones de escribir, eliminar, arrastrar y colocar, cortar y pegar. Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden rehacer.

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

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**rehacer EM \_**](em-redo.md)
</dt> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





