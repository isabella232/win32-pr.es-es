---
title: Código de notificación de NM_CUSTOMDRAW (encabezado) (commctrl. h)
description: Lo envía un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Controles de Windows de código de notificación de NM_CUSTOMDRAW (encabezado)
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658411"
---
# <a name="nm_customdraw-header-notification-code"></a>NM \_ código de notificación de CUSTOMDRAW (encabezado)

Lo envía un control de encabezado para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contiene información sobre la operación de dibujo. El miembro **dwItemSpec** de esta estructura contiene el índice del elemento que se está dibujando y el miembro **lItemlParam** de esta estructura contiene el *lParam* del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ predeterminado**</dt> </dl>         | El control se dibujará por sí mismo. No enviará ningún mensaje de [ \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                       |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario de cualquier operación de dibujo relacionada con los elementos. Enviará \_ los códigos de notificación de nm CUSTOMDRAW antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de que se dibuje un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versiones de control comunes](common-control-versions.md). El control notificará al elemento primario cuando se dibuje un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Consulte [uso de Draw personalizado](custom-draw.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





