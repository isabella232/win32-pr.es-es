---
description: Notifica a una Appbar cuando se ha producido un evento que puede afectar al tamaño y la posición de la Appbar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Mensaje de ABN_POSCHANGED (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984374"
---
# <a name="abn_poschanged-message"></a>Mensaje de ABN \_ POSCHANGED

Notifica a una Appbar cuando se ha producido un evento que puede afectar al tamaño y la posición de la Appbar. Los eventos incluyen cambios en el tamaño, la posición y el estado de visibilidad de la barra de tareas, así como la adición, eliminación o cambio de tamaño de otro Appbar en el mismo lado de la pantalla.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un Appbar debe responder a este mensaje de notificación mediante el envío de los mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) . Si su posición ha cambiado, el Appbar debe llamar a la función [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para moverse a la nueva posición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

