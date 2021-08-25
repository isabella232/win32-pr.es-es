---
title: MCM_SIZERECTTOMIN mensaje (Commctrl.h)
description: Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN controles de Windows mensaje
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
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799235"
---
# <a name="mcm_sizerecttomin-message"></a>Mensaje \_ DE MCM SIZERECTTOMIN

Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SizeRectToMin.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

En la entrada, contiene un puntero a una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) que describe una región mayor o igual que el tamaño necesario para ajustarse al número deseado de calendarios. Cuando esta función devuelve un resultado, contiene la estructura **RECT** mínima que se ajusta a este número de calendarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Sin usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

