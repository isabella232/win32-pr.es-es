---
title: Código de notificación de NM_CUSTOMDRAW (vista de árbol) (commctrl. h)
description: Lo envía un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- Código de notificación de NM_CUSTOMDRAW (vista de árbol) controles de Windows
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905002"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>NM \_ CUSTOMDRAW (vista de árbol) código de notificación

Lo envía un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) que contiene y recibe información sobre la operación de dibujo. El miembro **dwItemSpec** del miembro **nmcd** de esta estructura contiene el identificador del elemento que se está dibujando. El miembro **lItemlParam** del miembro **nmcd** de esta estructura contiene el *lParam* del elemento que se está dibujando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ predeterminado**</dt> </dl>         | El control se dibuja a sí mismo. No envía ningún código [ \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notifica al elemento primario de cualquier operación de dibujo relacionada con los elementos. Envía códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notifica al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notifica al elemento primario después de dibujar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4,71.](common-control-versions.md) El control notifica al elemento primario cuando se dibuja un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](custom-draw.md). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

[Versión 5,80.](common-control-versions.md) Si cambia la fuente devolviendo [**CDRF \_ NEWFONT**](cdrf-constants.md), el control de vista de árbol podría mostrar texto recortado. Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes. Si desea cambiar la fuente de un control de vista de árbol, obtendrá mejores resultados si envía un mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) con el valor de *wParam* establecido en 5 antes de agregar elementos al control.

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

 

 





