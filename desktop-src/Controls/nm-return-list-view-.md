---
title: NM_RETURN de notificación (vista de lista) (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- NM_RETURN (vista de lista) de código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167861"
---
# <a name="nm_return-list-view-notification-code"></a>Código de \_ notificación NM RETURN (vista de lista)

Notifica a la ventana primaria de un control de vista de lista que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





