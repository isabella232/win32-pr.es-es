---
title: MCM_SETCALENDARBORDER mensaje (Commctrl.h)
description: Establece el tamaño del borde, en píxeles. Puede enviar este mensaje explícitamente o mediante la \_ macro SetCalendarBorder de MonthCal.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697205"
---
# <a name="mcm_setcalendarborder-message"></a>Mensaje \_ SETCALENDARBORDER de MCM

Establece el tamaño del borde, en píxeles. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetCalendarBorder de MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si **es TRUE**, el tamaño del borde se establece en el número de píxeles que especifica *lParam.* Si **es FALSE**, el tamaño del borde se restablece al valor predeterminado especificado por el tema, o cero si no se usan temas.

</dd> <dt>

*lParam* 
</dt> <dd>

Número de píxeles del tamaño del borde.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





