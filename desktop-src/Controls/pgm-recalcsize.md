---
title: PGM_RECALCSIZE mensaje (Commctrl.h)
description: Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. Al enviar este mensaje, se enviará una notificación \_ PGN CALCSIZE. Puede enviar este mensaje explícitamente o usar la macro Pager \_ RecalcSize.
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
ms.openlocfilehash: 099f17af0cc4edc79df01fcb03864cdbf2879ae75df701f30f32610a50ae884d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540545"
---
# <a name="pgm_recalcsize-message"></a>Mensaje \_ DE PGM RECALCSIZE

Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. Al enviar este mensaje, se enviará una notificación [ \_ PGN CALCSIZE.](pgn-calcsize.md) Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ RecalcSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





