---
title: TTN_SHOW de notificación (Commctrl.h)
description: Notifica a la ventana de propietario que se va a mostrar un control de información sobre herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW código de notificación Windows controles
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408817"
---
# <a name="ttn_show-notification-code"></a>Código de notificación show de TTN \_

Notifica a la ventana de propietario que se va a mostrar un control de información sobre herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

[Versión 4.70.](common-control-versions.md) Para mostrar la información sobre herramientas en su ubicación predeterminada, devuelva cero. Para personalizar la posición de la información sobre herramientas, vuelva a colocar la ventana de información sobre herramientas con la [**función SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) y devuelva **TRUE.**

> [!Note]  
> Para las versiones anteriores a la 4.70, no hay ningún valor devuelto.

 

## <a name="remarks"></a>Comentarios

Un rectángulo de ventana de información sobre herramientas es algo mayor que su rectángulo de presentación de texto y su origen se desplaza hacia arriba y hacia la izquierda. Si necesita colocar con precisión el rectángulo de presentación de texto de una información sobre herramientas, el mensaje [**\_ ADJUSTRECT de TTM**](ttm-adjustrect.md) convierte un rectángulo de presentación de texto en el rectángulo de la ventana de información sobre herramientas correspondiente y viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

