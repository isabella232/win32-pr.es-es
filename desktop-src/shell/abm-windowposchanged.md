---
description: Notifica al sistema cuándo ha cambiado la posición de una barra de aplicaciones. Una barra de aplicaciones debe llamar a este mensaje en respuesta al mensaje \_ WINDOWPOSCHANGED de WM.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468309"
---
# <a name="abm_windowposchanged-message"></a>Mensaje \_ WINDOWPOSCHANGED de ABM

Notifica al sistema cuándo ha cambiado la posición de una barra de aplicaciones. Una barra de aplicaciones debe llamar a este mensaje en respuesta al [**mensaje \_ WINDOWPOSCHANGED de WM.**](/windows/desktop/winmsg/wm-windowposchanged)


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica la barra de aplicaciones que se va a activar. Debe especificar los **miembros cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

Este mensaje se omite si el **miembro hWnd** de la estructura a la que apunta *pabd* identifica una barra de aplicaciones autohide.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

