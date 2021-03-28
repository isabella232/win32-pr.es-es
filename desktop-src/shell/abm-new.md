---
description: Registra un nuevo Appbar y especifica el identificador de mensaje que el sistema debe usar para enviar mensajes de notificación. Un Appbar debe enviar este mensaje antes de enviar cualquier otro mensaje de Appbar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Mensaje de ABM_NEW (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808882"
---
# <a name="abm_new-message"></a>ABN \_ nuevo mensaje

Registra un nuevo Appbar y especifica el identificador de mensaje que el sistema debe usar para enviar mensajes de notificación. Un Appbar debe enviar este mensaje antes de enviar cualquier otro mensaje de Appbar.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de la ventana de la nueva Appbar y el identificador de mensaje. Debe especificar los miembros **cbSize**, **hWnd** y **uCallbackMessage** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** si se produce un error o si el Appbar ya está registrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




