---
title: Mensaje de WM_SYSKEYUP (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando el usuario suelta una tecla que se presionó mientras se mantenía presionada la tecla ALT.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Entrada de mouse y teclado de mensaje de WM_SYSKEYUP
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
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362010"
---
# <a name="wm_syskeyup-message"></a>Mensaje de SYSKEYUP de WM \_

Se envía a la ventana con el foco de teclado cuando el usuario suelta una tecla que se presionó mientras se mantenía presionada la tecla ALT. También se produce cuando no hay ninguna ventana que tenga actualmente el foco de teclado; en este caso, el mensaje de **\_ SYSKEYUP de WM** se envía a la ventana activa. La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el parámetro *lParam* .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de tecla virtual de la clave que se va a liberar. Consulte [**códigos de tecla virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Número de repeticiones del mensaje actual. El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla. El número de repeticiones siempre es uno para un mensaje de **\_ SYSKEYUP de WM** .         |
| 16-23 | Código de recorrido. El valor depende del OEM.                                                                                                                                                                                  |
| 24    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es cero.                   |
| 25-28 | Sector No use.                                                                                                                                                                                                         |
| 29    | Código de contexto. El valor es 1 si la tecla ALT está presionada mientras se suelta la tecla; es cero si el mensaje **de \_ SYSKEYUP de WM** se envía a la ventana activa porque ninguna ventana tiene el foco de teclado. |
| 30    | Estado de la clave anterior. El valor es siempre 1 para un mensaje de **\_ SYSKEYUP de WM** .                                                                                                                                                 |
| 31    | Estado de transición. El valor es siempre 1 para un mensaje de **\_ SYSKEYUP de WM** .                                                                                                                                                   |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior si se liberó la tecla F10 o la tecla Alt. El parámetro *wParam* del mensaje se establece en **SC \_ KEYMENU**.

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.

Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

Para los que no son de U. S. Teclados de clave mejorada 102, la tecla ALT derecha se trata como una tecla CTRL + ALT. En la tabla siguiente se muestra la secuencia de mensajes que se produce cuando el usuario presiona y suelta esta clave.



| Message                           | Código de tecla virtual |
|-----------------------------------|------------------|
| [**KEYDOWN de WM \_**](wm-keydown.md) | **\_control VK**  |
| [**KEYDOWN de WM \_**](wm-keydown.md) | **\_menú VK**     |
| [**KEYUP de WM \_**](wm-keyup.md)     | **\_control VK**  |
| **SYSKEYUP de WM \_**                  | **\_menú VK**     |



 

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

[**SYSKEYDOWN de WM \_**](wm-syskeydown.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

