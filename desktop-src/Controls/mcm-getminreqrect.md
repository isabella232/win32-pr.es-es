---
title: MCM_GETMINREQRECT mensaje (Commctrl.h)
description: Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro \_ MonthCal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT controles de Windows mensaje
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
ms.openlocfilehash: 575636837b1485de62dd5e603a0dea38455c4c99926c13f3bd05101fe2a27eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062055"
---
# <a name="mcm_getminreqrect-message"></a>Mensaje \_ GETMINREQRECT de MCM

Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetMinReqRect.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibirá información de rectángulo delimitador. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero *y lParam* recibe la información de límite aplicable si se realiza correctamente. De lo contrario, el mensaje devuelve cero.

## <a name="remarks"></a>Comentarios

El tamaño mínimo de ventana necesario para un control de calendario mensual depende de la fuente, los estilos de control, las métricas del sistema y la configuración regional seleccionados actualmente. Cuando una aplicación cambia cualquier cosa que afecte al tamaño mínimo de la ventana o procese un mensaje [**\_ WM SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) debe enviar **MCM \_ GETMINREQRECT** para determinar el nuevo tamaño mínimo.

> [!Note]  
> El rectángulo devuelto **por MCM \_ GETMINREQRECT** no incluye el ancho de la cadena "Today", si está presente. Si no se establece el estilo [**\_ MCS NOTODAY,**](month-calendar-control-styles.md) la aplicación también debe recuperar el rectángulo que define el ancho de cadena "Today" enviando un mensaje [**\_ GETMAXTODAYWIDTH de MCM.**](mcm-getmaxtodaywidth.md) Use el mayor de los dos rectángulos para asegurarse de que no se recorta la cadena "Today".

 

Los **miembros** superior **e izquierdo** de la estructura a la que apunta *lParam* siempre serán cero. Los **miembros derecho** e **inferior** representan el *mínimo cx* y *cy* necesarios para el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

