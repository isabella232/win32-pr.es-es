---
title: NM_CUSTOMDRAW de notificación (barra de seguimiento) (Commctrl.h)
description: Enviado por un control trackbar para notificar a sus ventanas primarias sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW de notificación (barra de seguimiento) Windows controles
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d863b180948676342a49615a526c8f6860905744aaf5269468807ad6dc04fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109555"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>Código \_ de notificación DE NM CUSTOMDRAW (barra de seguimiento)

Enviado por un control trackbar para notificar a sus ventanas primarias sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El **miembro dwItemSpec** de esta estructura contendrá uno de los valores [de](custom-draw-values.md) dibujo personalizados que indica qué parte del control se está dibujando. Los controles Trackbar insertan los siguientes valores en el **miembro dwItemSpec** de esta estructura para identificar la parte del control que se está dibujando:



| Value                                                                                                                                                      | Significado                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**CANAL \_ TBCD**</dt> </dl> | Identifica el canal en el que se desliza el marcador de posición del control de la barra de seguimiento. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifica el marcador de posición del control trackbar. Esta es la parte del control que mueve el usuario. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica las marcas de graduación de incremento que aparecen a lo largo del borde del control trackbar. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que puede devolver la aplicación depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW asociada**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibujará a sí mismo. No enviará ningún código de notificación [DE NM \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación NM \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4.71.](common-control-versions.md) El control notificará al elemento primario cuando se dibuja un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambiar fuentes y colores.](custom-draw.md) Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación ha dibujado el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/>                                                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar dibujo personalizado](custom-draw.md)
</dt> </dl>

 

 





