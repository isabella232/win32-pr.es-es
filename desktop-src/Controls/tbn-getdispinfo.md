---
title: TBN_GETDISPINFO de notificación (Commctrl.h)
description: Recupera la información para mostrar de un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO código de notificación Windows controles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ffa2afafee64a82fb440d3d1e3031899ab94c0614d32449062ca29426aaa6a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876855"
---
# <a name="tbn_getdispinfo-notification-code"></a>Código de notificación \_ GETDISPINFO de TBN

Recupera la información para mostrar de un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBDISPINFO.**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) El **miembro idCommand** especifica el identificador de comando del elemento, el **miembro lParam** contiene los datos definidos por la aplicación del elemento y el **miembro dwMask** especifica qué información se solicita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETDISPINFOW** (Unicode) y **TBN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





