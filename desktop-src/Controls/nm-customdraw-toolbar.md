---
title: NM_CUSTOMDRAW de notificación (barra de herramientas) (Commctrl.h)
description: Enviado por una barra de herramientas para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- NM_CUSTOMDRAW de notificación (barra de herramientas) de Windows controles
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
ms.openlocfilehash: 5d3e12f0c0db15c0200f28701f85d72606faf3938d53e5feb92495826f0edd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061735"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>Código de notificación DE NM \_ CUSTOMDRAW (barra de herramientas)

Enviado por una barra de herramientas para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versión 4.70.](common-control-versions.md) Puntero a una [**estructura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El **miembro dwItemSpec** de esta estructura contiene el identificador de comando del elemento que se está dibujando. El **miembro lItemlParam** de esta estructura contiene el **valor dwData** del elemento que se va a dibujar.

[Versión 4.71.](common-control-versions.md) Puntero a una [**estructura NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) que contiene información sobre la operación de dibujo. El **miembro dwItemSpec** del **miembro nmcd** de esta estructura contiene el identificador de comando del elemento que se está dibujando. El **miembro lItemlParam** del **miembro nmcd** de esta estructura contiene el **valor dwData** del elemento que se está dibujando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW asociada**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibujará a sí mismo. No enviará ningún código de notificación [ADICIONAL DE NM \_ CUSTOMDRAW](nm-customdraw.md) para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4.71.](common-control-versions.md) El control notificará al elemento primario cuando se dibuja un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambio de fuentes y colores.](custom-draw.md) Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación hizo que el elemento se dibujara manualmente. El control no dibujará el elemento. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |
| <dl> <dt>**BLENDICON DE TBCDRF \_**</dt> </dl>       | [Versión 5.00.](common-control-versions.md) Combine el botón al 50 por ciento con el fondo. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NOBACKGROUND**</dt> </dl>    | [Versión 5.00.](common-control-versions.md) No dibuje el fondo del botón. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NOEDGES**</dt> </dl>         | [Versión 4.71.](common-control-versions.md) No dibuje bordes de botón. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                             |
| <dl> <dt>**TBCDRF \_ HILITEHOTTRACK**</dt> </dl>  | [Versión 4.71.](common-control-versions.md) Use el **miembro clrHighlightHotTrack de** la estructura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) para dibujar el fondo de los elementos de seguimiento activo. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                        |
| <dl> <dt>**TBCDRF \_ NOOFFSET**</dt> </dl>        | [Versión 4.71.](common-control-versions.md) No desfase el botón cuando se presiona. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                |
| <dl> <dt>**TBCDRF \_ NOMARK**</dt> </dl>          | No dibuje el resaltado predeterminado de los elementos que tengan [**el valor TBSTATE \_ MARCADO.**](toolbar-button-states.md) Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                              |
| <dl> <dt>**TBCDRF \_ NOETCHEDEFFECT**</dt> </dl>  | [Versión 4.71.](common-control-versions.md) No dibuje el efecto grabado para los elementos deshabilitados. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                         |
| <dl> <dt>**TBCDRF \_ USECDCOLORS**</dt> </dl>     | [Versión 6.00,](common-control-versions.md) **solo Windows Vista.** Use colores de dibujo personalizados para representar texto independientemente del estilo visual.<br/>                                                                                                                                         |



 

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

 

 





