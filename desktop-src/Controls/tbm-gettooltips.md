---
title: TBM_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador del control de información sobre herramientas asignado a la barra de seguimiento, si lo hay.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078069"
---
# <a name="tbm_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de TBM

Recupera el identificador del control de información sobre herramientas asignado a la barra de seguimiento, si lo hay.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas asignado a la barra de seguimiento o **NULL** si la información sobre herramientas no está en uso. Si el control trackbar no usa el estilo [**TBS \_ TOOLTIPS,**](trackbar-control-styles.md) el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





