---
title: WM_SYSKEYDOWN mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258039"
---
# <a name="wm_syskeydown-message"></a>Mensaje \_ SYSKEYDOWN de WM

Se publica en la ventana con el foco del teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla. También se produce cuando ninguna ventana tiene actualmente el foco del teclado; En este caso, el **mensaje \_ SYSKEYDOWN** de WM se envía a la ventana activa. La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el *parámetro lParam.*


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la tecla que se está pulsando. Consulte [**Códigos de clave virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que se autorpeda la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficientemente larga, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo. |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Reservado; no se usan.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si la tecla ALT está presionada mientras se presiona la tecla . es 0 si el mensaje **\_ WM SYSKEYDOWN** se publica en la ventana activa porque ninguna ventana tiene el foco del teclado.                                                                  |
| 30    | Estado de la clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.                                                                                                                                                    |
| 31    | Estado de transición. El valor siempre es 0 para un **mensaje \_ SYSKEYDOWN de WM.**                                                                                                                                                                                         |

Para obtener más información, vea [Marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina la clave especificada y genera un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) wm si la clave es TAB o ENTRAR.

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco del teclado.

Debido a la repetición automática, puede producirse más de un mensaje **\_ SYSKEYDOWN de WM** antes de que se envíe un mensaje [**\_ SYSKEYUP**](wm-syskeyup.md) de WM. El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje **\_ SYSKEYDOWN** de WM indica la primera transición hacia abajo o una transición hacia abajo repetida.

Para los teclados mejorados de 101 y 102 teclas, las teclas mejoradas son las teclas ALT y CTRL correctas en la sección principal del teclado. las teclas de dirección INS, DEL, HOME, END, PAGE UP, PAGE DOWN y en los clústeres situados a la izquierda del teclado numérico. y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de tecla extendida en el *parámetro lParam.*

Este mensaje también se envía cada vez que el usuario presiona la tecla F10 sin la tecla ALT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

