---
title: Código de notificación de NM_CUSTOMDRAW (commctrl. h)
description: Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW controles de código de notificación de Windows
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489047"
---
# <a name="nm_customdraw-notification-code"></a>Código de notificación de NM \_ CUSTOMDRAW

Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura personalizada relacionada con Draw que contiene información sobre la operación de dibujo. En la lista siguiente se especifican los controles y sus estructuras asociadas.



| Control                     | Estructura de dibujo personalizada                    |
|-----------------------------|------------------------------------------|
| Rebar, TrackBar y header | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Vista de lista                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| Información sobre herramientas                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Vista de árbol                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Barra de herramientas                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ predeterminado**</dt> </dl>         | El control se dibujará por sí mismo. No enviará códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) adicionales para este ciclo de pintura. Esta marca no se puede usar con ningún otro marcador. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_**</dt> </dl>           | El control solo dibujará el fondo.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos. Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control enviará un código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) cuando se complete el ciclo de dibujo para todo el control. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | La aplicación recibirá un código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT \| CDDS \_ SubItem antes de que se dibuje cada subelemento de vista de lista. Después, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF de \_ forma predeterminada**](cdrf-constants.md) para el procesamiento predeterminado. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | El control no dibujará el rectángulo de foco alrededor de un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

Actualmente, los siguientes controles admiten la funcionalidad de dibujo personalizada: encabezado, vista de lista, Rebar, barra de herramientas, información sobre herramientas, TrackBar y vista de árbol. El dibujo personalizado también se admite para los controles de botón si tiene un manifiesto de aplicación para asegurarse de que Comctl32.dll versión 6 esté disponible.

Si este mensaje se trata en un procedimiento de cuadro de diálogo, debe establecer el valor devuelto como parte de los datos de la ventana antes de devolver **true**. Para obtener más información, vea [**función dialogproc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Vista**
</dt> <dt>

[Dibujo personalizado](custom-draw.md)
</dt> </dl>

 

