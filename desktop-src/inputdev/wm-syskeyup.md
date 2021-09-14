---
title: WM_SYSKEYUP mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando el usuario suelta una tecla presionada mientras se mantiene presionada la tecla ALT.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241563"
---
# <a name="wm_syskeyup-message"></a>Mensaje \_ SYSKEYUP de WM

Se publica en la ventana con el foco del teclado cuando el usuario suelta una tecla presionada mientras se mantiene presionada la tecla ALT. También se produce cuando ninguna ventana tiene actualmente el foco del teclado; En este caso, el **mensaje \_ SYSKEYUP** de WM se envía a la ventana activa. La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el *parámetro lParam.*

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la clave que se va a liberar. Consulte [**Códigos de clave virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que se autorepeta la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. El recuento de repeticiones siempre es uno para un **mensaje \_ SYSKEYUP de WM.**         |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                  |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; de lo contrario, es cero.                   |
| 25-28 | Reservado; no use.                                                                                                                                                                                                         |
| 29    | Código de contexto. El valor es 1 si la tecla ALT está abajo mientras se libera la clave; es cero si el **mensaje \_ SYSKEYUP** de WM se publica en la ventana activa porque ninguna ventana tiene el foco del teclado. |
| 30    | Estado de clave anterior. El valor siempre es 1 para un **mensaje \_ SYSKEYUP de WM.**                                                                                                                                                 |
| 31    | Estado de transición. El valor siempre es 1 para un **mensaje \_ SYSKEYUP de WM.**                                                                                                                                                   |

Para obtener más información, vea [Marcas de mensaje de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM a la ventana de nivel superior si se ha liberado la tecla F10 o la tecla ALT. El *parámetro wParam* del mensaje se establece en **SC \_ KEYMENU.**

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco del teclado.

En el caso de los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT y CTRL correctas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow de los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de clave extendida en el *parámetro lParam.*

Para usuarios que no son de EE. UU. Teclados mejorados de 102 teclas, la tecla ALT derecha se controla como una tecla CTRL+ALT. En la tabla siguiente se muestra la secuencia de mensajes que resultan cuando el usuario presiona y suelta esta tecla.



| Message                           | Código de clave virtual |
|-----------------------------------|------------------|
| [**WM \_ KEYDOWN**](wm-keydown.md) | **VK \_ CONTROL**  |
| [**WM \_ KEYDOWN**](wm-keydown.md) | **MENÚ \_ DE VK**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **VK \_ CONTROL**  |
| **WM \_ SYSKEYUP**                  | **MENÚ \_ DE VK**     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

