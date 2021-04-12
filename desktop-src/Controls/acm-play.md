---
title: Mensaje de ACM_PLAY (commctrl. h)
description: Reproduce un clip AVI en un control Animation. El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede enviar este mensaje explícitamente o mediante el uso de la macro Animate \_ Play.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489652"
---
# <a name="acm_play-message"></a>Mensaje de reproducción de ACM \_

Reproduce un clip AVI en un control Animation. El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede enviar este mensaje explícitamente o mediante el uso de la macro [**Animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un valor **uint** que especifica el número de veces que se va a reproducir el clip AVI. Un valor de-1 significa que se reproduce el clip indefinidamente.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el índice de base cero del marco en el que comienza la reproducción. El valor debe ser menor que 65.536. Un valor de cero significa que comienza con el primer fotograma del clip AVI.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es el índice de base cero del marco en el que finaliza la reproducción. El valor debe ser menor que 65.536. Un valor de-1 significa terminar con el último fotograma del clip AVI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Puede usar [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) para dirigir el control de animación y mostrar un fotograma determinado del clip AVI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

