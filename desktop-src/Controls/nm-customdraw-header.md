---
title: NM_CUSTOMDRAW (encabezado) de notificación (Commctrl.h)
description: Enviado por un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- NM_CUSTOMDRAW (encabezado) de notificación de Windows controles
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
ms.openlocfilehash: d099a3cc951715af00569de7463148af28eb977c9081800543802015c38c4582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914885"
---
# <a name="nm_customdraw-header-notification-code"></a>Código de notificación DE NM \_ CUSTOMDRAW (encabezado)

Enviado por un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El **miembro dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el **miembro lItemlParam** de esta estructura contiene *el lParam del elemento.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW asociada**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibujará a sí mismo. No enviará ningún mensaje [ADICIONAL DE NM \_ CUSTOMDRAW](nm-customdraw.md) para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                       |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de notificación NM CUSTOMDRAW antes y después \_ de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versiones de control comunes](common-control-versions.md). El control notificará al elemento primario cuando se dibuja un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambio de fuentes y colores.](custom-draw.md) Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación hizo que el elemento se dibujara manualmente. El control no dibujará el elemento. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentarios

Consulte [Uso del dibujo personalizado para](custom-draw.md) obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





