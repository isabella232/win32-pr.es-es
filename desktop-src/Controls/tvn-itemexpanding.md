---
title: Código de notificación de TVN_ITEMEXPANDING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997015"
---
# <a name="tvn_itemexpanding-notification-code"></a>Código de notificación de ITEMEXPANDING de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . El miembro **itemNew** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento primario en los miembros **hItem**, **State** y **lParam** . El miembro de **acción** indica si la lista debe expandirse o contraerse. Para obtener una lista de los valores posibles, vea la descripción del mensaje de [**\_ expansión TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para evitar que la lista se expanda o contraiga.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) y **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





