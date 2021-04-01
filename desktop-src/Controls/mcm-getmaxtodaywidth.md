---
title: Mensaje de MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Recupera el ancho máximo del 0034; actualmente \ 0034; cadena en un control de calendario mensual. Esto incluye el texto de la etiqueta y el texto de la fecha. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802515"
---
# <a name="mcm_getmaxtodaywidth-message"></a>Mensaje de MCM \_ GETMAXTODAYWIDTH

Recupera el ancho máximo de la cadena "Today" en un control de calendario mensual. Esto incluye el texto de la etiqueta y el texto de la fecha. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de la cadena "Today", en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





