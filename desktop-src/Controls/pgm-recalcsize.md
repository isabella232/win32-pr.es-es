---
title: PGM_RECALCSIZE mensaje (Commctrl.h)
description: Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. Al enviar este mensaje, se enviará una notificación \_ PGN CALCSIZE. Puede enviar este mensaje explícitamente o usar la \_ macro Pager RecalcSize.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167697"
---
# <a name="pgm_recalcsize-message"></a>Mensaje \_ PGM RECALCSIZE

Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. Al enviar este mensaje, se enviará una [notificación \_ PGN CALCSIZE.](pgn-calcsize.md) Puede enviar este mensaje explícitamente o usar la macro [**\_ Pager RecalcSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





