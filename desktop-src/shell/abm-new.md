---
description: Registra una nueva barra de aplicaciones y especifica el identificador de mensaje que el sistema debe usar para enviarle mensajes de notificación. Una barra de aplicaciones debe enviar este mensaje antes de enviar cualquier otro mensaje de la barra de aplicaciones.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468310"
---
# <a name="abm_new-message"></a>Mensaje ABM \_ NEW

Registra una nueva barra de aplicaciones y especifica el identificador de mensaje que el sistema debe usar para enviarle mensajes de notificación. Una barra de aplicaciones debe enviar este mensaje antes de enviar cualquier otro mensaje de la barra de aplicaciones.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de ventana y el identificador de mensaje de la nueva barra de aplicaciones. Debe especificar los **miembros cbSize**, **hWnd** y **uCallbackMessage** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza **correctamente** o FALSE si se produce un error o si la barra de aplicaciones ya está registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




