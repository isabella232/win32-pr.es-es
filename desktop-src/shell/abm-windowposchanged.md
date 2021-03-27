---
description: Notifica al sistema cuando ha cambiado la posición de una Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de WINDOWPOSCHANGED de WM \_ .
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Mensaje de ABM_WINDOWPOSCHANGED (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497050"
---
# <a name="abm_windowposchanged-message"></a>ABN \_ WINDOWPOSCHANGED

Notifica al sistema cuando ha cambiado la posición de una Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de [**\_ WINDOWPOSCHANGED de WM**](/windows/desktop/winmsg/wm-windowposchanged) .


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica el Appbar que se va a activar. Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Este mensaje se omite si el miembro **hWnd** de la estructura a la que apunta *pabd* identifica un Appbar de ocultación automáticamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

