---
title: Mensaje de MCM_GETMINREQRECT (commctrl. h)
description: Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489964"
---
# <a name="mcm_getminreqrect-message"></a>Mensaje de MCM \_ GETMINREQRECT

Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá información del rectángulo delimitador. Este parámetro debe ser una dirección válida y no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero y *lParam* recibe la información de límite aplicable si se realiza correctamente. De lo contrario, el mensaje devuelve cero.

## <a name="remarks"></a>Observaciones

El tamaño mínimo de ventana necesario para un control de calendario mensual depende de la fuente, los estilos de control, las métricas del sistema y la configuración regional seleccionados actualmente. Cuando una aplicación cambia todo lo que afecta al tamaño mínimo de la ventana o procesa un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) , debe enviar **MCM \_ GETMINREQRECT** para determinar el nuevo tamaño mínimo.

> [!Note]  
> El rectángulo devuelto por **MCM \_ GETMINREQRECT** no incluye el ancho de la cadena "Today", si está presente. Si no se establece el estilo [**MCS \_ noactual**](month-calendar-control-styles.md) , la aplicación también debe recuperar el rectángulo que define el ancho de la cadena "Today" mediante el envío de un mensaje [**\_ GETMAXTODAYWIDTH de MCM**](mcm-getmaxtodaywidth.md) . Utilice el mayor de los dos rectángulos para asegurarse de que la cadena "Today" no se recorte.

 

Los miembros **superior** e **izquierdo** de la estructura a la que apunta *lParam* siempre serán cero. Los miembros **derecho** e **inferior** representan el mínimo de *CX* y *CY* necesarios para el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

