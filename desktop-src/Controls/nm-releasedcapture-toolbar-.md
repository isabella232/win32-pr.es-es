---
title: NM_RELEASEDCAPTURE de notificación (barra de herramientas) (Commctrl.h)
description: Notifica a la ventana primaria de un control de barra de herramientas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- NM_RELEASEDCAPTURE (barra de herramientas) de código de notificación Windows Controles
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
ms.openlocfilehash: d915b3af073ba0c6b5c74a7b13317f7b2d4ab8a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167882"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>Código de \_ notificación NM RELEASEDCAPTURE (barra de herramientas)

Notifica a la ventana primaria de un control de barra de herramientas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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



 

 





