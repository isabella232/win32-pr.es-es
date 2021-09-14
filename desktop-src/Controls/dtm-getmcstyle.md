---
title: DTM_GETMCSTYLE mensaje (Commctrl.h)
description: Obtiene el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la \_ macro DateTime GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892324"
---
# <a name="dtm_getmcstyle-message"></a>Mensaje \_ GETMCSTYLE de DTM

Obtiene el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro [**\_ DateTime GetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo del control. Para obtener más información, vea [Estilos de control de calendario mensual](month-calendar-control-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





