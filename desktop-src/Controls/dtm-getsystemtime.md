---
title: DTM_GETSYSTEMTIME mensaje (Commctrl.h)
description: Obtiene la hora seleccionada actualmente de un control selector de fecha y hora (DTP) y la coloca en una estructura SYSTEMTIME especificada. Puede enviar este mensaje explícitamente o usar la macro DateTime \_ GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273372"
---
# <a name="dtm_getsystemtime-message"></a>Mensaje GETSYSTEMTIME de DTM \_

Obtiene la hora seleccionada actualmente de un control selector de fecha y hora (DTP) y la coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ GetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) Si **DTM \_ GETSYSTEMTIME devuelve** GDT \_ VALID, esta estructura contendrá la hora seleccionada actualmente. De lo contrario, no contendrá información válida. Este parámetro debe ser un puntero válido; no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve GDT VALID si la información de hora se ha colocado \_ correctamente *en lParam.* Devuelve GDT NONE si el control se estableció en el estilo \_ [**\_ DTS SHOWNONE**](date-and-time-picker-control-styles.md) y no se ha seleccionado la casilla de control. Devuelve error de GDT \_ si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

