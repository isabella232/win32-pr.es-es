---
title: ACM_PLAY mensaje (Commctrl.h)
description: Reproduce un clip AVI en un control de animación. El control reproduce el clip en segundo plano mientras el subproceso continúa ejecutándose. Puede enviar este mensaje explícitamente o mediante la macro Animar \_ reproducción.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072333"
---
# <a name="acm_play-message"></a>Mensaje play de ACM \_

Reproduce un clip AVI en un control de animación. El control reproduce el clip en segundo plano mientras el subproceso continúa ejecutándose. Puede enviar este mensaje explícitamente o mediante la macro [**Animar \_ reproducción.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

UINT **que** especifica el número de veces que se reproducirá el clip AVI. Un valor de -1 significa reproducir el clip indefinidamente.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el índice de base cero del marco donde comienza la reproducción. El valor debe ser menor que 65 536. Un valor de cero significa comenzar con el primer fotograma del clip AVI.

[**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el índice de base cero del marco donde termina la reproducción. El valor debe ser menor que 65 536. Un valor de -1 significa finalizar con el último fotograma del clip AVI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Puede usar [**Animate \_ Seek para**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) dirigir el control de animación para mostrar un fotograma determinado del clip AVI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

