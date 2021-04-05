---
title: Código de notificación de LVN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento está cambiando. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997184"
---
# <a name="lvn_itemchanging-notification-code"></a>Código de notificación de ITEMCHANGING de LVN \_

Notifica a la ventana primaria de un control de vista de lista que un elemento está cambiando. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica el elemento y especifica cuál de sus atributos está cambiando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para evitar el cambio o **false** para permitir el cambio.

## <a name="remarks"></a>Observaciones

Si el control de vista de lista tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , \_ no se envían los códigos de notificación de LVN ITEMCHANGING.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





