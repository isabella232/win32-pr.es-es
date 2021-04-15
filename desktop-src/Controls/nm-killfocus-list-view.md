---
title: Código de notificación de NM_KILLFOCUS (vista de lista) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- NM_KILLFOCUS (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489040"
---
# <a name="nm_killfocus-list-view-notification-code"></a>NM \_ KILLFOCUS (vista de lista) código de notificación

Notifica a la ventana primaria de un control de vista de lista que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





