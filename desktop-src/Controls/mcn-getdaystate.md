---
title: Código de notificación de MCN_GETDAYSTATE (commctrl. h)
description: Enviado por un control de calendario mensual para solicitar información acerca de cómo deben mostrarse los días individuales. Este código de notificación solo se envía por los controles de calendario mensual que usan el \_ estilo MCS DAYSTATE y se envía en forma de un mensaje de notificación de WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802419"
---
# <a name="mcn_getdaystate-notification-code"></a>Código de notificación de GETDAYSTATE de MCN \_

Enviado por un control de calendario mensual para solicitar información acerca de cómo deben mostrarse los días individuales. Este código de notificación solo se envía por los controles de calendario mensual que usan el estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) y se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) . La estructura contiene información sobre el período de tiempo para el que el control necesita información y recibe la dirección de una matriz que proporciona estos datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El control de este código de notificación permite que la aplicación Personalice su presentación especificando que determinados días se muestran en negrita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





