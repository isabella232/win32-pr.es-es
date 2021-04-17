---
title: Mensaje de WM_SYSKEYDOWN (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Entrada de mouse y teclado de mensaje de WM_SYSKEYDOWN
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695939"
---
# <a name="wm_syskeydown-message"></a>Mensaje de SYSKEYDOWN de WM \_

Se envía a la ventana con el foco de teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla. También se produce cuando no hay ninguna ventana que tenga actualmente el foco de teclado; en este caso, el mensaje de **\_ SYSKEYDOWN de WM** se envía a la ventana activa. La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el parámetro *lParam* .


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de tecla virtual de la tecla que se va a presionar. Consulte [**códigos de tecla virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Número de repeticiones del mensaje actual. El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla. Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes. Sin embargo, el número de repeticiones no es acumulativo. |
| 16-23 | Código de recorrido. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Sector No use.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si la tecla ALT está presionada mientras se presiona la tecla; es 0 si el mensaje **de \_ SYSKEYDOWN de WM** se envía a la ventana activa porque ninguna ventana tiene el foco de teclado.                                                                  |
| 30    | Estado de la clave anterior. El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.                                                                                                                                                    |
| 31    | Estado de transición. El valor es siempre 0 para un mensaje de **\_ SYSKEYDOWN de WM** .                                                                                                                                                                                         |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina la clave especificada y genera un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) si la clave es TAB o entrar.

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.

Debido a la repetición automática, se puede producir más de un mensaje de **WM \_ SYSKEYDOWN** antes de que se envíe un mensaje de [**\_ SYSKEYUP de WM**](wm-syskeyup.md) . El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje de **\_ SYSKEYDOWN de WM** indica la primera transición hacia abajo o una transición hacia abajo.

Para los teclados mejorados de la clave 101-y 102, las teclas mejoradas son las teclas ALT y CTRL adecuadas en la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

Este mensaje también se envía cuando el usuario presiona la tecla F10 sin la tecla ALT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**SYSCOMMAND de WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**SYSKEYUP de WM \_**](wm-syskeyup.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

