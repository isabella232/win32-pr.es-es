---
title: TBN_GETDISPINFO de notificación (Commctrl.h)
description: Recupera la información de visualización de un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO código de notificación Windows controles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166349"
---
# <a name="tbn_getdispinfo-notification-code"></a>Código de notificación \_ GETDISPINFO de TBN

Recupera la información de visualización de un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBDISPINFO.**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) El **miembro idCommand** especifica el identificador de comando del elemento, el miembro **lParam** contiene los datos definidos por la aplicación del elemento y el miembro **dwMask** especifica qué información se solicita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETDISPINFOW** (Unicode) y **TBN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





