---
description: Notifica a una barra de aplicaciones cuando se ha producido un evento que puede afectar al tamaño y la posición de la barra de aplicaciones.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943605"
---
# <a name="abn_poschanged-message"></a>Mensaje \_ ABN POSCHANGED

Notifica a una barra de aplicaciones cuando se ha producido un evento que puede afectar al tamaño y la posición de la barra de aplicaciones. Los eventos incluyen cambios en el tamaño, la posición y el estado de visibilidad de la barra de tareas, así como la adición, eliminación o cambio de tamaño de otra barra de aplicaciones en el mismo lado de la pantalla.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una barra de aplicaciones debe responder a este mensaje de notificación enviando los mensajes [**\_ ABM QUERYPOS**](abm-querypos.md) y [**ABM \_ SETPOS.**](abm-setpos.md) Si su posición ha cambiado, la barra de aplicaciones debe llamar a la [**función MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para moverse a la nueva posición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

