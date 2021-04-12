---
title: Mensaje de MCM_GETCALID (commctrl. h)
description: Obtiene el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150405"
---
# <a name="mcm_getcalid-message"></a>Mensaje de MCM \_ GETCALID

Obtiene el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .

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

IDENTIFICADOR del calendario actual. Una de las constantes de los [identificadores de calendario](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

