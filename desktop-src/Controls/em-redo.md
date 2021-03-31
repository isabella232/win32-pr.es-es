---
title: Mensaje EM_REDO (RichEdit. h)
description: Envía un \_ mensaje de rehacer em a un control Rich Edit para rehacer la siguiente acción en la cola de puesta al día del control.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491494"
---
# <a name="em_redo-message"></a>\_Mensaje de rehacer em

Envía un mensaje de **\_ rehacer em** a un control Rich Edit para rehacer la siguiente acción en la cola de puesta al día del control.

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

Si la operación de **rehacer** se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación de **rehacer** , el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Para determinar si hay alguna acción en la cola de rehacer del control, envíe el mensaje [**\_ CANREDO em**](em-canredo.md) .

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

[**de \_ em**](em-canredo.md)
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> </dl>

 

 





