---
title: TBN_INITCUSTOMIZE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166333"
---
# <a name="tbn_initcustomize-notification-code"></a>Código de notificación \_ TBN INITCUSTOMIZE

Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve TBNRF \_ HIDEHELP para suprimir el botón Ayuda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





