---
description: El IME envía a una aplicación para notificar a la aplicación una versión de clave y para mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: WM_IME_KEYUP mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65d80876643cc27136223c112c1e045bc797adbd0bf160adda1c3cea894767e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102075"
---
# <a name="wm_ime_keyup-message"></a>Mensaje KEYUP de WM \_ IME \_

El IME envía a una aplicación para notificar a la aplicación una versión de clave y para mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la clave.

</dd> <dt>

*lParam* 
</dt> <dd>

Recuento de repeticiones, código de examen, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, como se muestra a continuación.



| bit   | Significado                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones. Este valor siempre es 1.                                       |
| 16-23 | Examinar código.                                                                  |
| 24    | Clave extendida. Este valor es 1 si es una clave extendida. De lo contrario, es 0. |
| 25-28 | No se usa.                                                                   |
| 29    | Código de contexto. Este valor siempre es 0.                                       |
| 30    | Estado de clave anterior. Este valor siempre es 1.                                 |
| 31    | Estado de transición. Este valor siempre es 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver 0 si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Una aplicación puede procesar este mensaje o pasarlo a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para generar un [**mensaje KEYUP de WM \_ correspondiente.**](../inputdev/wm-keyup.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del Administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
