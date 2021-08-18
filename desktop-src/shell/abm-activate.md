---
description: Notifica al sistema que se ha activado una barra de aplicaciones. Una barra de aplicaciones debe llamar a este mensaje en respuesta al mensaje WM \_ ACTIVATE.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224f04a88a1e69a1a67fc08c6018d33af2bcdbc6f34ff9fbd00d1dd76f82ce5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461138"
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

## <a name="remarks"></a>Comentarios

Este mensaje se omite si el **miembro hWnd** de la estructura a la que apunta *pabd* identifica una barra de aplicaciones autohide. El sistema establece automáticamente el orden Z para mostrar automáticamente las barras de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

