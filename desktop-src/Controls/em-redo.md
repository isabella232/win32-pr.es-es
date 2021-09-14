---
title: EM_REDO mensaje (Richedit.h)
description: Envía un mensaje EM REDO a un control de edición enriquecido para volver a hacer la siguiente acción en la cola \_ de rehacer del control.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062151"
---
# <a name="em_redo-message"></a>Mensaje \_ DE REDO DE EM

Envía un **mensaje \_ EM REDO** a un control de edición enriquecido para volver a hacer la siguiente acción en la cola de rehacer del control.

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

Si la **operación de rehacer** se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error **en la** operación de rehacer, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Para determinar si hay alguna acción en la cola de rehacer del control, envíe el mensaje [**EM \_ CANREDO.**](em-canredo.md)

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

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





