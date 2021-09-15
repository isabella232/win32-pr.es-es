---
description: Notifica al sistema que se ha activado una barra de aplicaciones. Una barra de aplicaciones debe llamar a este mensaje en respuesta al mensaje WM \_ ACTIVATE.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468311"
---
# <a name="abm_activate-message"></a>Mensaje ACTIVATE de ABM \_

Notifica al sistema que se ha activado una barra de aplicaciones. Una barra de aplicaciones debe llamar a este mensaje en respuesta al [**mensaje WM \_ ACTIVATE.**](/windows/desktop/inputdev/wm-activate)


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
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

Este mensaje se omite si el **miembro hWnd** de la estructura a la que apunta *pabd* identifica una barra de aplicaciones autohide. El sistema establece automáticamente el orden Z para mostrar automáticamente las barras de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

