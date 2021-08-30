---
title: EM_CANREDO mensaje (Richedit.h)
description: Determina si hay alguna acción en la cola de rehacer del control.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8898ba469d52e4098c2430dff5234a3522a6fbd3569bec823ff776a3f1c420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916055"
---
# <a name="em_canredo-message"></a>Mensaje \_ DE EM CANREDO

Determina si hay alguna acción en la cola de rehacer del control.

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

Si hay acciones en la cola de rehacer del control, el valor devuelto es distinto de cero.

Si la cola de puesta al día está vacía, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Para rehacer la operación de deshacer más reciente, envíe el mensaje [**\_ EM REDO.**](em-redo.md)

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

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**REDO DE EM \_**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





