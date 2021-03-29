---
title: Código de notificación de TVN_SELCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED controles de código de notificación de Windows
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
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905581"
---
# <a name="tvn_selchanged-notification-code"></a>Código de notificación de SELCHANGED de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que la selección ha cambiado de un elemento a otro. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Los miembros **itemOld** y **itemNew** de la estructura **NMTREEVIEW** son estructuras [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contienen información sobre el elemento seleccionado anteriormente y el elemento recién seleccionado. Solo los miembros **Mask**, **hItem**, **State** e **lParam** de estas estructuras son válidos. Los miembros de **stateMask** de las estructuras **TVITEM** especificados por **itemOld** y **itemNew** no están definidos en la entrada. El miembro de **acción** de la estructura **NMTREEVIEW** indica el tipo de acción que provocó el cambio de la selección. Puede ser uno de los siguientes valores:



| Requisito | Value |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Mediante una pulsación de tecla.   |
| TVC \_ BYMOUSE    | Con un clic del mouse. |
| TVC \_ desconocido    | Desconocido.          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) y **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





