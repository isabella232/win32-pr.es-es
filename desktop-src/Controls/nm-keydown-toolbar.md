---
title: NM_KEYDOWN de notificación (barra de herramientas) (Commctrl.h)
description: 'NM_KEYDOWN (barra de herramientas): se envía mediante un control cuando el control tiene el foco del teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN código de notificación (barra de herramientas) Windows controles
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a937969b325de881caa97cd2a67d7c11056aa5542d0cd92c751d1ff42a569b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958134"
---
# <a name="nm_keydown-toolbar-notification-code"></a>Código de \_ notificación NM KEYDOWN (barra de herramientas)

Lo envía un control cuando el control tiene el foco del teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que produjo el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar que el control procese la clave, o bien cero en caso contrario.

## <a name="remarks"></a>Comentarios

Actualmente, solo el control de barra de herramientas envía este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





