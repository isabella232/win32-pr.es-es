---
title: Mensaje de MCM_SETCALID (commctrl. h)
description: Establece el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079005"
---
# <a name="mcm_setcalid-message"></a>Mensaje de MCM \_ SETCALID

Establece el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

IDENTIFICADOR del calendario. Una de las constantes de los [identificadores de calendario](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Sin usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

