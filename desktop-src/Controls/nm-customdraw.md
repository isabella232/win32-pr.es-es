---
title: NM_CUSTOMDRAW de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW de notificación Windows controles
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
ms.openlocfilehash: ff8f1a7fe570d88ce583bc0d0aaa34576f8c440836060904d182559e46c3950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078919"
---
# <a name="nm_customdraw-notification-code"></a>Código de notificación DE NM \_ CUSTOMDRAW

Notifica a la ventana primaria de un control las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

Puntero a una estructura personalizada relacionada con el dibujo que contiene información sobre la operación de dibujo. En la lista siguiente se especifican los controles y sus estructuras asociadas.



| Control                     | Estructura de dibujo personalizada                    |
|-----------------------------|------------------------------------------|
| Rebar, trackbar y header | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Vista de lista                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| Información sobre herramientas                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Vista de árbol                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Barra de herramientas                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW asociada**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibujará a sí mismo. No enviará códigos de notificación [ \_ adicionales de NM CUSTOMDRAW](nm-customdraw.md) para este ciclo de pintura. Esta marca no se puede usar con ninguna otra marca. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | El control solo dibujará el fondo.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambio de fuentes y colores.](custom-draw.md) Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control enviará un código [de notificación NM \_ CUSTOMDRAW](nm-customdraw.md) cuando se complete el ciclo de dibujo de todo el control. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | La aplicación recibirá un código de notificación [ \_ NM CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT CDDS SUBITEM antes de dibujar cada subelemento de vista \| \_ de lista. A continuación, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF \_ DODEFAULT**](cdrf-constants.md) para el procesamiento predeterminado. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación hizo que el elemento se dibujara manualmente. El control no dibujará el elemento. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | El control no dibujará el rectángulo de foco alrededor de un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentarios

Actualmente, los siguientes controles admiten la funcionalidad de dibujo personalizada: encabezado, vista de lista, rebar, barra de herramientas, información sobre herramientas, barra de seguimiento y vista de árbol. El dibujo personalizado también se admite para los controles de botón si tiene un manifiesto de aplicación para asegurarse de que Comctl32.dll versión 6 está disponible.

Si este mensaje se controla en un procedimiento de diálogo, debe establecer el valor devuelto como parte de los datos de la ventana antes de devolver **TRUE**. Para obtener más información, vea [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Conceptual**
</dt> <dt>

[Dibujo personalizado](custom-draw.md)
</dt> </dl>

 

