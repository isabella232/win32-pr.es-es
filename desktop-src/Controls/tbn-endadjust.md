---
title: TBN_ENDADJUST de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha dejado de personalizar una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166366"
---
# <a name="tbn_endadjust-notification-code"></a>Código de notificación \_ ENDADJUST de TBN

Notifica a la ventana primaria de una barra de herramientas que el usuario ha dejado de personalizar una barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_ENDADJUST 

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



 

 





