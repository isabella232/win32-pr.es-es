---
title: WM_KEYUP mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando se libera una tecla que no es del sistema. Una tecla no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT o una tecla de teclado que se presiona cuando una ventana tiene el foco del teclado.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468819"
---
# <a name="wm_keyup-message"></a>Mensaje \_ DE WM KEYUP

Se publica en la ventana con el foco del teclado cuando se libera una tecla que no es del sistema. Una tecla no del sistema es una tecla  que se presiona cuando no se presiona la tecla ALT o una tecla de teclado que se presiona cuando una ventana tiene el foco del teclado.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la clave no del sistema. Consulte [Códigos de clave virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que se autorpeda la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. El recuento de repeticiones siempre es 1 para un **mensaje \_ WM KEYUP.** |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                     |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; de lo contrario, es 0.         |
| 25-28 | Reservado; no se usan.                                                                                                                                                                                            |
| 29    | Código de contexto. El valor siempre es 0 para un **mensaje \_ WM KEYUP.**                                                                                                                                             |
| 30    | Estado de la clave anterior. El valor siempre es 1 para un **mensaje \_ WM KEYUP.**                                                                                                                                       |
| 31    | Estado de transición. El valor siempre es 1 para un **mensaje \_ WM KEYUP.**                                                                                                                                         |

Para obtener más información, vea [Marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM a la ventana de nivel superior si se ha liberado la tecla F10 o la tecla ALT. El *parámetro wParam* del mensaje se establece en SC \_ KEYMENU.

Para los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT y CTRL derechas en la sección principal del teclado. las teclas de dirección INS, DEL, HOME, END, PAGE UP, PAGE DOWN y en los clústeres situados a la izquierda del teclado numérico. y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de tecla extendida en el *parámetro lParam.*

Las aplicaciones deben *pasar wParam* [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sin modificarlo en absoluto.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

