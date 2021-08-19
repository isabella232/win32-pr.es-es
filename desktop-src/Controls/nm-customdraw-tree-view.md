---
title: NM_CUSTOMDRAW de notificación (vista de árbol) (Commctrl.h)
description: Enviado por un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW de notificación (vista de árbol) Windows controles
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
ms.openlocfilehash: 9571d8461b43cebe047d80933af53a0c1aa1b865ede6280b8de2a33b74a60f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088845"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>Código \_ de notificación DE NM CUSTOMDRAW (vista de árbol)

Enviado por un control de vista de árbol para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) que contiene y recibe información sobre la operación de dibujo. El **miembro dwItemSpec** del **miembro nmcd** de esta estructura contiene el identificador del elemento que se está dibujando. El **miembro lItemlParam** del **miembro nmcd** de esta estructura contiene *el lParam* del elemento que se está dibujando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que la aplicación puede devolver depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibuja a sí mismo. No envía ningún código [ \_ CUSTOMDRAW NM](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notifica al elemento primario las operaciones de dibujo relacionadas con elementos. Envía códigos [de \_ notificación NM CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notifica al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notifica al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4.71.](common-control-versions.md) El control notifica al elemento primario cuando se dibuja un subelemento de vista de lista. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambiar fuentes y colores.](custom-draw.md) Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación ha dibujado el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentarios

[Versión 5.80.](common-control-versions.md) Si cambia la fuente devolviendo [**CDRF \_ NEWFONT,**](cdrf-constants.md)el control de vista de árbol podría mostrar texto recortado. Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes. Si desea cambiar la fuente de un control de vista de árbol, se obtienen mejores resultados si envía un mensaje [**\_ SETVERSION**](ccm-setversion.md) de CCM con el valor *wParam* establecido en 5 antes de agregar cualquier elemento al control.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar dibujo personalizado](custom-draw.md)
</dt> </dl>

 

 





