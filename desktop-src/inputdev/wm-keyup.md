---
title: Mensaje de WM_KEYUP (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando se suelta una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT o una tecla del teclado presionada cuando una ventana tiene el foco de teclado.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Entrada de mouse y teclado de mensaje de WM_KEYUP
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422193"
---
# <a name="wm_keyup-message"></a>\_Mensaje KEYUP de WM

Se envía a la ventana con el foco de teclado cuando se suelta una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando *no* se presiona la tecla Alt o una tecla del teclado presionada cuando una ventana tiene el foco de teclado.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de tecla virtual de la clave que no es del sistema. Consulte [códigos de tecla virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Número de repeticiones del mensaje actual. El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla. El número de repeticiones es siempre 1 para un mensaje de **\_ KEYUP de WM** . |
| 16-23 | Código de recorrido. El valor depende del OEM.                                                                                                                                                                     |
| 24    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es 0.         |
| 25-28 | Sector No use.                                                                                                                                                                                            |
| 29    | Código de contexto. El valor siempre es 0 para un mensaje de **\_ KEYUP de WM** .                                                                                                                                             |
| 30    | Estado de la clave anterior. El valor es siempre 1 para un mensaje de **\_ KEYUP de WM** .                                                                                                                                       |
| 31    | Estado de transición. El valor es siempre 1 para un mensaje de **\_ KEYUP de WM** .                                                                                                                                         |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior si se liberó la tecla F10 o la tecla Alt. El parámetro *wParam* del mensaje se establece en SC \_ KEYMENU.

Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

Las aplicaciones deben pasar *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sin modificarlo.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**KEYDOWN de WM \_**](wm-keydown.md)
</dt> <dt>

[**SYSCOMMAND de WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

