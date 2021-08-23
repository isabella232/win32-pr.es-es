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
ms.openlocfilehash: 30b1398d843711e868a6b5b96cf6a66893bf74fef1e50bfdd61fa36f81f05c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611325"
---
# <a name="wm_syskeydown-message"></a>Mensaje \_ SYSKEYDOWN de WM

Se publica en la ventana con el foco del teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla. También se produce cuando ninguna ventana tiene actualmente el foco del teclado; En este caso, el **mensaje \_ SYSKEYDOWN de WM** se envía a la ventana activa. La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el *parámetro lParam.*


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
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que se autorepeta la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficiente, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo. |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; De lo contrario, es 0.                                                              |
| 25-28 | Reservado; no use.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si la tecla ALT está presionada mientras se presiona la tecla . es 0 si el mensaje **\_ SYSKEYDOWN** de WM se publica en la ventana activa porque ninguna ventana tiene el foco del teclado.                                                                  |
| 30    | Estado de clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.                                                                                                                                                    |
| 31    | Estado de transición. El valor siempre es 0 para un **mensaje \_ SYSKEYDOWN de WM.**                                                                                                                                                                                         |

Para obtener más información, vea [Marcas de mensaje de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina la clave especificada y genera un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM si la clave es TAB o ENTER.

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco del teclado.

Debido a la repetición automática, se puede producir más de un **mensaje \_ SYSKEYDOWN de WM** antes de que se envíe un mensaje [**\_ SYSKEYUP**](wm-syskeyup.md) de WM. El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje **\_ SYSKEYDOWN** de WM indica la primera transición hacia abajo o una transición hacia abajo repetida.

En el caso de los teclados mejorados de 101 y 102 teclas, las teclas mejoradas son las teclas ALT y CTRL correctas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow de los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de clave extendida en el *parámetro lParam.*

Este mensaje también se envía cada vez que el usuario presiona la tecla F10 sin la tecla ALT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

