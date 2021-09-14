---
title: SBN_SIMPLEMODECHANGE de notificación (Commctrl.h)
description: Enviado por un control de barra de estado cuando cambia el modo simple debido a un mensaje SB \_ SIMPLE. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE de notificación Windows controles
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167057"
---
# <a name="sbn_simplemodechange-notification-code"></a>Código de notificación \_ SIMPLEMODECHANGE de SBN

Enviado por un control de barra de estado cuando cambia el modo simple debido a un [**mensaje SB \_ SIMPLE.**](sb-simple.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La barra de estado omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





