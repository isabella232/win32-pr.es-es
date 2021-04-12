---
title: Código de notificación de LVN_DELETEITEM (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151283"
---
# <a name="lvn_deleteitem-notification-code"></a>Código de notificación de LVN \_ DELETEITEM

Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . El miembro **iItem** identifica el elemento que se va a eliminar. Si el control no tiene el estilo **LVS \_ OWNERDATA** , *lParam* son los datos definidos por la aplicación asociados al elemento. Todos los demás miembros de esta estructura son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No agregue, elimine ni reorganice los elementos de la vista de lista mientras procesa este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





