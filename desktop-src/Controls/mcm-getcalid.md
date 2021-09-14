---
title: MCM_GETCALID mensaje (Commctrl.h)
description: Obtiene el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la \_ macro MonthCal GetPROCD.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362567"
---
# <a name="mcm_getcalid-message"></a>Mensaje \_ GET HAND de MCM

Obtiene el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetPROCD.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Identificador del calendario actual. Una de las [constantes de identificadores de](/windows/desktop/Intl/calendar-identifiers) calendario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

