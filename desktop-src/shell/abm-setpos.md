---
description: Establece el tamaño y la posición de la pantalla de una barra de aplicaciones.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861607"
---
# <a name="abm_setpos-message"></a>Mensaje de SETPOS de ABM \_

Establece el tamaño y la posición de la pantalla de una barra de aplicaciones. El mensaje especifica un borde de pantalla y el rectángulo delimitador para la barra de aplicaciones. El sistema puede ajustar el rectángulo delimitador para que la barra de aplicaciones no interfiera con la Windows de tareas ni con ninguna otra barra de aplicaciones.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) El **miembro uEdge** especifica un borde de pantalla y el **miembro rc** contiene el rectángulo delimitador. Cuando se [**devuelve la función SHAppBarMessage,**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) **rc** contiene el rectángulo delimitador aprobado. Debe especificar los **miembros cbSize**, **hWnd,** **uEdge** y **rc** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

Este mensaje hace que el sistema envíe el mensaje de [**notificación \_ POSCHANGED**](abn-poschanged.md) de ABN a todas las barras de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




