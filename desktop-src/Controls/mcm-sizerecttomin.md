---
title: Mensaje de MCM_SIZERECTTOMIN (commctrl. h)
description: Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151053"
---
# <a name="mcm_sizerecttomin-message"></a>Mensaje de MCM \_ SIZERECTTOMIN

Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

En la entrada, contiene un puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que describe una región que es mayor o igual que el tamaño necesario para ajustarse al número deseado de calendarios. Cuando esta función devuelve un valor, contiene la estructura **Rect** mínima que se ajusta a este número de calendarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Sin usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

