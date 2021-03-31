---
title: Mensaje de DTM_GETMCSTYLE (commctrl. h)
description: Obtiene el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro GetMonthCalStyle de fecha y hora \_ .
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996756"
---
# <a name="dtm_getmcstyle-message"></a>DTM \_ GETMCSTYLE

Obtiene el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la [**macro \_ GetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo del control. Para obtener más información, vea [estilos de control de calendario mensual](month-calendar-control-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





