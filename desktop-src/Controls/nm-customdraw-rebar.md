---
title: Código de notificación de NM_CUSTOMDRAW (rebar) (commctrl. h)
description: Lo envía el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Código de notificación NM_CUSTOMDRAW (rebar) controles de Windows
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151267"
---
# <a name="nm_customdraw-rebar-notification-code"></a>Código de notificación de NM \_ CUSTOMDRAW (rebar)

Lo envía el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** de esta estructura contiene el identificador de la banda que se está dibujando. El miembro **lItemlParam** de esta estructura contiene el *lParam* de la banda que se está dibujando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ predeterminado**</dt> </dl>         | El control se dibujará por sí mismo. No enviará ninguna notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos. Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                           |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de que se dibuje un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                               |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos. Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                           |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información acerca de cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

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

 

 





