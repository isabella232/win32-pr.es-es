---
description: El mensaje SYSCOLORCHANGE de WM se envía a todas las ventanas de nivel superior cuando se realiza un cambio \_ en una configuración de color del sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: WM_SYSCOLORCHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e39ff8b5189da1a4cf48b7f6923c1cf12e8f30aa20fb26457d54a3f01d1b5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118483104"
---
# <a name="wm_syscolorchange-message"></a>Mensaje \_ SYSCOLORCHANGE de WM

El **mensaje \_ SYSCOLORCHANGE de WM** se envía a todas las ventanas de nivel superior cuando se realiza un cambio en una configuración de color del sistema.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El sistema envía un [**mensaje \_ WM PAINT**](wm-paint.md) a cualquier ventana afectada por un cambio de color del sistema.

Las aplicaciones que tienen pinceles que usan los colores del sistema existentes deben eliminar esos pinceles y volver a crearlos con los nuevos colores del sistema.

Las ventanas de nivel superior que usan controles comunes deben reenviar el mensaje **\_ SYSCOLORCHANGE** de WM a los controles; de lo contrario, los controles no recibirán una notificación del cambio de color. Esto garantiza que los colores usados por los controles comunes sean coherentes con los que usan otros objetos de interfaz de usuario. Por ejemplo, un control de barra de herramientas usa el color "Objetos 3D" para dibujar sus botones. Si el usuario cambia el color de objetos 3D pero el mensaje **\_ SYSCOLORCHANGE** de WM no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecerán en su color original mientras cambia el color de otros botones del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Mensajes de color](color-messages.md)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
