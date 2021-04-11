---
description: Se envía a una aplicación mediante el IME para notificar a la aplicación de una pulsación de tecla y mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Mensaje de WM_IME_KEYDOWN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275443"
---
# <a name="wm_ime_keydown-message"></a>\_Mensaje de KEYDOWN IME de WM \_

Se envía a una aplicación mediante el IME para notificar a la aplicación de una pulsación de tecla y mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Código de tecla virtual de la clave.

</dd> <dt>

*lParam* 
</dt> <dd>

Recuento de repeticiones, código de recorrido, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, tal como se muestra en la tabla siguiente.



| bit   | Significado                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones.                                                               |
| 16-23 | Examinar código.                                                                  |
| 24    | Clave extendida. Este valor es 1 si es una clave extendida. De lo contrario, es 0. |
| 25-28 | No se utiliza.                                                                   |
| 29    | Código de contexto. Este valor siempre es 0.                                       |
| 30    | Estado de clave anterior. Este valor es 1 si la tecla está presionada o 0 si está activa.    |
| 31    | Estado de transición. Este valor siempre es 0.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver 0 si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Una aplicación puede procesar este mensaje o pasarlo a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para generar un mensaje [**\_ KEYDOWN de WM**](../inputdev/wm-keydown.md) coincidente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
