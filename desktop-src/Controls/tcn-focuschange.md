---
title: TCN_FOCUSCHANGE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de pestaña que el foco del botón ha cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166178"
---
# <a name="tcn_focuschange-notification-code"></a>Código de notificación DE TCN \_ FOCUSCHANGE

Notifica a la ventana primaria de un control de pestaña que el foco del botón ha cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





