---
title: TBN_TOOLBARCHANGE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha personalizado una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- TBN_TOOLBARCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166306"
---
# <a name="tbn_toolbarchange-notification-code"></a>TBN \_ TOOLBARCHANGE notification code

Notifica a la ventana primaria de la barra de herramientas que el usuario ha personalizado una barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





