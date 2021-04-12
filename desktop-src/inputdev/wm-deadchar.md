---
title: Mensaje de WM_DEADCHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje de KEYUP de WM.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- Entrada de mouse y teclado de mensaje de WM_DEADCHAR
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490055"
---
# <a name="wm_deadchar-message"></a>Mensaje de DEADCHAR de WM \_

Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje de [**\_ KEYUP de WM**](wm-keyup.md) . **WM \_ DEADCHAR** especifica un código de carácter generado por una tecla muerta. Una tecla muerta es una tecla que genera un carácter, como diéresis (doble punto), que se combina con otro carácter para formar un carácter compuesto. Por ejemplo, el carácter diéresis-O () se genera escribiendo la tecla muerta para el carácter de diéresis y, a continuación, escribiendo la tecla O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter generado por la clave muerta.

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
| 29    | Código de contexto. El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.                                                                                                                                                     |
| 30    | Estado de la clave anterior. El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.                                                                                                                                                    |
| 31    | Estado de transición. El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.                                                                                                                                                            |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones usan el mensaje de **\_ DEADCHAR de WM** para proporcionar los comentarios del usuario sobre cada tecla presionada. Por ejemplo, una aplicación puede mostrar el acento en la posición del carácter actual sin mover el símbolo de intercalación.

Dado que no hay necesariamente una correspondencia uno a uno entre las claves presionadas y los mensajes de caracteres generados, la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) más reciente que precede a la publicación del mensaje de **\_ DEADCHAR de WM** .

Para los teclados mejorados de clave 101-y 102, las teclas extendidas son la ALT derecha y las teclas CTRL derecha en la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**KEYDOWN de WM \_**](wm-keydown.md)
</dt> <dt>

[**KEYUP de WM \_**](wm-keyup.md)
</dt> <dt>

[**SYSDEADCHAR de WM \_**](wm-sysdeadchar.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

