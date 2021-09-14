---
title: NM_THEMECHANGED de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el tema ha cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167821"
---
# <a name="nm_themechanged-notification-code"></a>Código de \_ notificación NM THEMECHANGED

Notifica a la ventana primaria de un control que el tema ha cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





