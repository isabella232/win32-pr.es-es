---
title: IPM_SETRANGE mensaje (Commctrl.h)
description: Establece el intervalo válido para el campo especificado en el control de direcciones IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE controles de Windows mensaje
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
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434475"
---
# <a name="ipm_setrange-message"></a>Mensaje \_ SETRANGE de IPM

Establece el intervalo válido para el campo especificado en el control de direcciones IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de campo de base cero al que se aplicará el intervalo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **WORD** que contiene el límite inferior del intervalo en el byte de orden inferior y el límite superior en el byte de orden superior. Ambos valores son inclusivos. La [**macro MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) también se puede usar para crear el intervalo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

Si el usuario escribe un valor en el campo que está fuera de este intervalo, el control enviará la notificación [ \_ FIELDCHANGED](ipn-fieldchanged.md) de IPN con el valor especificado. Si el valor sigue fuera del intervalo después de enviar la notificación, el control intentará cambiar el valor especificado al límite de intervalo más cercano.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





