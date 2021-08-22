---
title: TVN_SELCHANGED de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957784"
---
# <a name="tvn_selchanged-notification-code"></a>Código de notificación \_ DE TVN SELCHANGED

Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Los **miembros itemOld** y **itemNew** de la estructura **NMTREEVIEW** son estructuras [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contienen información sobre el elemento seleccionado previamente y el elemento recién seleccionado. Solo los **miembros mask**, **hItem**, **state** y **lParam** de estas estructuras son válidos. Los **miembros stateMask** de las estructuras **TVITEM** especificados por **itemOld** y **itemNew** no están definidos en la entrada. El **miembro** de acción de la **estructura NMTREEVIEW** indica el tipo de acción que hizo que la selección cambiara. Puede ser uno de los siguientes valores:



| Requisito | Value |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Mediante una pulsación de tecla.   |
| TVC \_ BYMOUSE    | Con un clic del mouse. |
| TVC \_ UNKNOWN    | Desconocido.          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) y **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





