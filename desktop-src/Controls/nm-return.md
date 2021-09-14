---
title: NM_RETURN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- NM_RETURN código de notificación Windows controles
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
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167854"
---
# <a name="nm_return-notification-code"></a>Código de \_ notificación DE NM RETURN

Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





