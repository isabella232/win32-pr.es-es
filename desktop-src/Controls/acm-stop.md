---
title: ACM_STOP mensaje (Commctrl.h)
description: Detiene la reproducción de un clip AVI en un control de animación. Puede enviar este mensaje explícitamente o mediante la macro Animar \_ detener.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- ACM_STOP controles de Windows mensaje
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 210936d102cdf7c55f25106ec5f6dc8e962c3af7679e6c5294ea10b6e833c8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079409"
---
# <a name="acm_stop-message"></a>Mensaje STOP de ACM \_

Detiene la reproducción de un clip AVI en un control de animación. Puede enviar este mensaje explícitamente o mediante la macro [**Animar \_ detener.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





