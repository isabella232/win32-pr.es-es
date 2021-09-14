---
title: NM_RDBLCLK (pestaña) código de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- NM_RDBLCLK (pestaña) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167922"
---
# <a name="nm_rdblclk-tab-notification-code"></a>Código de notificación DE NM \_ RDBLCLK (pestaña)

Notifica a la ventana primaria de un control de pestaña que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para no permitir el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





