---
title: Código de notificación de NM_CUSTOMDRAW (barra de herramientas) (commctrl. h)
description: Enviado por una barra de herramientas para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- Código de notificación de NM_CUSTOMDRAW (barra de herramientas) controles de Windows
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535638"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>NM \_ CUSTOMDRAW (barra de herramientas) código de notificación

Enviado por una barra de herramientas para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versión 4,70](common-control-versions.md). Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** de esta estructura contiene el identificador de comando del elemento que se está dibujando. El miembro **lItemlParam** de esta estructura contiene el valor de **dwData** para el elemento que se está dibujando.

[Versión 4,71](common-control-versions.md). Puntero a una estructura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** del miembro **nmcd** de esta estructura contiene el identificador de comando del elemento que se está dibujando. El miembro **lItemlParam** del miembro **nmcd** de esta estructura contiene el valor **dwData** del elemento que se está dibujando.

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
| <dl> <dt>**TBCDRF \_ BLENDICON**</dt> </dl>       | [Versión 5,00](common-control-versions.md). Mezcle el botón 50 por ciento con el fondo. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NObackground**</dt> </dl>    | [Versión 5,00](common-control-versions.md). No dibuje el fondo del botón. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NOedges**</dt> </dl>         | [Versión 4,71](common-control-versions.md). No dibuje bordes de botón. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                             |
| <dl> <dt>**TBCDRF \_ HILITEHOTTRACK**</dt> </dl>  | [Versión 4,71](common-control-versions.md). Use el miembro **clrHighlightHotTrack** de la estructura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) para dibujar el fondo de los elementos de los que se hace un seguimiento completo. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                        |
| <dl> <dt>**TBCDRF \_ NOoffset**</dt> </dl>        | [Versión 4,71](common-control-versions.md). No desplace el botón cuando esté presionado. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                |
| <dl> <dt>**TBCDRF \_ NOmarca**</dt> </dl>          | No dibuje el resaltado predeterminado de los elementos que tienen el [**TBSTATE \_ marcado**](toolbar-button-states.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                              |
| <dl> <dt>**TBCDRF \_ NOETCHEDEFFECT**</dt> </dl>  | [Versión 4,71](common-control-versions.md). No dibuje efectos grabados para los elementos deshabilitados. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                         |
| <dl> <dt>**TBCDRF \_ USECDCOLORS**</dt> </dl>     | [Versión 6,00](common-control-versions.md), solo **Windows Vista** . Use dibujar colores personalizados para representar el texto independientemente del estilo visual.<br/>                                                                                                                                         |



 

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

 

 





