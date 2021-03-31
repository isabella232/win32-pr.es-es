---
title: Mensaje de MCM_SETCALENDARBORDER (commctrl. h)
description: Establece el tamaño del borde, en píxeles. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER controles de mensajes de Windows
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
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490517"
---
# <a name="mcm_setcalendarborder-message"></a>Mensaje de MCM \_ SETCALENDARBORDER

Establece el tamaño del borde, en píxeles. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si es **true**, el tamaño del borde se establece en el número de píxeles que *lParam* especifica. Si es **false**, el tamaño del borde se restablece en el valor predeterminado especificado por el tema, o bien, cero si no se usan los temas.

</dd> <dt>

*lParam* 
</dt> <dd>

Número de píxeles del tamaño del borde.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





