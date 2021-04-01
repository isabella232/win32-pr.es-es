---
title: Código de notificación de NM_CUSTOMDRAW (TrackBar) (commctrl. h)
description: Enviado por un control TrackBar para notificar a sus ventanas principales las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (TrackBar)
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151266"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>Código de notificación de NM \_ CUSTOMDRAW (TrackBar)

Enviado por un control TrackBar para notificar a sus ventanas principales las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** de esta estructura contendrá uno de los [valores de dibujo personalizados](custom-draw-values.md) que indica qué parte del control se está dibujando. Los controles TrackBar insertan los valores siguientes en el miembro **dwItemSpec** de esta estructura para identificar la parte del control que se está dibujando:



| Value                                                                                                                                                      | Significado                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifica el canal en el que se desplaza el marcador de control de la barra de desplazamiento. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**\_Thumb TBCD**</dt> </dl>       | Identifica el marcador de control de la barra de desplazamiento. Esta es la parte del control que mueve el usuario. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ las marcas**</dt> </dl>          | Identifica las marcas de graduación de incremento que aparecen a lo largo del borde del control TrackBar. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ predeterminado**</dt> </dl>         | El control se dibujará por sí mismo. No enviará ningún código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos. Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de que se dibuje un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4,71](common-control-versions.md). El control notificará al elemento primario cuando se dibuje un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar Draw personalizado](custom-draw.md)
</dt> </dl>

 

 





