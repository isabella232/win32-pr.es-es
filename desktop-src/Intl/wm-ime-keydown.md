---
description: El IME envía a una aplicación para notificar a la aplicación una pulsación de tecla y para mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: WM_IME_KEYDOWN mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535315"
---
# <a name="wm_ime_keydown-message"></a>Mensaje \_ KEYDOWN de WM IME \_

El IME envía a una aplicación para notificar a la aplicación una pulsación de tecla y para mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Recuento de repeticiones, código de examen, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, como se muestra en la tabla siguiente.



| bit   | Significado                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones.                                                               |
| 16-23 | Examinar código.                                                                  |
| 24    | Clave extendida. Este valor es 1 si es una clave extendida. De lo contrario, es 0. |
| 25-28 | No se usa.                                                                   |
| 29    | Código de contexto. Este valor siempre es 0.                                       |
| 30    | Estado de clave anterior. Este valor es 1 si la clave está abajo o 0 si está arriba.    |
| 31    | Estado de transición. Este valor siempre es 0.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver 0 si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Una aplicación puede procesar este mensaje o pasarlo a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para generar un [**mensaje KEYDOWN de WM \_ correspondiente.**](../inputdev/wm-keydown.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 
