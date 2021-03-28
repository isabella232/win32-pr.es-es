---
description: El mensaje de SYSCOLORCHANGE de WM \_ se envía a todas las ventanas de nivel superior cuando se realiza un cambio en la configuración de color del sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Mensaje de WM_SYSCOLORCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986055"
---
# <a name="wm_syscolorchange-message"></a>Mensaje de SYSCOLORCHANGE de WM \_

El mensaje de **\_ SYSCOLORCHANGE de WM** se envía a todas las ventanas de nivel superior cuando se realiza un cambio en la configuración de color del sistema.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

## <a name="remarks"></a>Observaciones

El sistema envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) a cualquier ventana afectada por un cambio de color del sistema.

Las aplicaciones que tienen pinceles que usan los colores del sistema existentes deben eliminar esos pinceles y volver a crearlos con los nuevos colores del sistema.

Las ventanas de nivel superior que usan controles comunes deben reenviar el mensaje de **\_ SYSCOLORCHANGE de WM** a los controles; de lo contrario, los controles no recibirán una notificación del cambio de color. Esto garantiza que los colores utilizados por los controles comunes son coherentes con los utilizados por otros objetos de la interfaz de usuario. Por ejemplo, un control de barra de herramientas usa el color "objetos 3D" para dibujar sus botones. Si el usuario cambia el color de los objetos 3D, pero el mensaje de **\_ SYSCOLORCHANGE de WM** no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecen en su color original mientras que el color de otros botones del sistema cambia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Mensajes de color](color-messages.md)
</dt> <dt>

[**pintura de WM \_**](wm-paint.md)
</dt> </dl>

 

 
