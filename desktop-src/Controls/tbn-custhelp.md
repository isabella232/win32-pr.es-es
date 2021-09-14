---
title: TBN_CUSTHELP de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha elegido el botón Ayuda en el cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166386"
---
# <a name="tbn_custhelp-notification-code"></a>Código de notificación \_ CUSTHELP de TBN

Notifica a la ventana primaria de una barra de herramientas que el usuario ha elegido el botón Ayuda en el cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_CUSTHELP 

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



 

 





