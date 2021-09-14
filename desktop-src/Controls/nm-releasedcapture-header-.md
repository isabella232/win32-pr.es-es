---
title: NM_RELEASEDCAPTURE (encabezado) de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: fca57009-dc96-4575-8c64-c753884b05fe
keywords:
- NM_RELEASEDCAPTURE (encabezado) de notificación de Windows controles
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
ms.openlocfilehash: 88334b9eb9791ee20be4b9defd6e979f788c5067
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167901"
---
# <a name="nm_releasedcapture-header-notification-code"></a>Código \_ de notificación NM RELEASEDCAPTURE (encabezado)

Notifica a la ventana primaria de un control de encabezado que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

El control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





