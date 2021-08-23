---
title: HDN_DIVIDERDBLCLICK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha hecho doble clic en el área divisora del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9ba7e974ce9e3adac2b48815bfb9bba5273db8298bc9948164be5904dca8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544681"
---
# <a name="hdn_dividerdblclick-notification-code"></a>Código de notificación \_ DIVIDERDBLCLICK de HDN

Notifica a la ventana primaria de un control de encabezado que el usuario ha hecho doble clic en el área divisora del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER que**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contiene información sobre el control de encabezado y el elemento cuyo divisor se hizo doble clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ DIVIDERDBLCLICKW** (Unicode) y **HDN \_ DIVIDERDBLCLICKA** (ANSI)<br/>   |



 

 





