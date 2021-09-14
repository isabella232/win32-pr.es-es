---
title: NM_RELEASEDCAPTURE (paginar) código de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- NM_RELEASEDCAPTURE (paginación) de código de notificación Windows Controles
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167893"
---
# <a name="nm_releasedcapture-pager-notification-code"></a>Código \_ de notificación NM RELEASEDCAPTURE (pager)

Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control de paginación omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





