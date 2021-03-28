---
description: Notifica al sistema que se ha activado un Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de activación de WM \_ .
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Mensaje de ABM_ACTIVATE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153928"
---
# <a name="abm_activate-message"></a>ABN \_ Activar mensaje

Notifica al sistema que se ha activado un Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de [**\_ activación de WM**](/windows/desktop/inputdev/wm-activate) .


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
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

Este mensaje se omite si el miembro **hWnd** de la estructura a la que apunta *pabd* identifica un Appbar de ocultación automáticamente. El sistema establece automáticamente el orden z para la ocultación automática de appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

