---
title: Mensaje de IPM_SETRANGE (commctrl. h)
description: Establece el intervalo válido para el campo especificado en el control de dirección IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079620"
---
# <a name="ipm_setrange-message"></a>\_Mensaje IPM SetRange

Establece el intervalo válido para el campo especificado en el control de dirección IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de campo basado en cero al que se aplicará el intervalo.

</dd> <dt>

*lParam* 
</dt> <dd>

Un valor de **palabra** que contiene el límite inferior del intervalo en el byte de orden inferior y el límite superior del byte de orden superior. Ambos valores son inclusivos. La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) también se puede usar para crear el intervalo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Si el usuario especifica un valor en el campo que está fuera de este intervalo, el control enviará la notificación [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) con el valor especificado. Si el valor todavía está fuera del intervalo después de enviar la notificación, el control intentará cambiar el valor especificado al límite de intervalo más cercano.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





