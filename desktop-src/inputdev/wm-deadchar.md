---
title: WM_DEADCHAR mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando la función TranslateMessage traduce un mensaje \_ WM KEYUP.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR entrada de teclado y mouse
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
ms.openlocfilehash: 4e4921d399c4a1c7a86596bfcc907b52d9c834235d133d6455b88c5a5a40c89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778755"
---
# <a name="wm_deadchar-message"></a>Mensaje \_ DEADCHAR de WM

Se publica en la ventana con el foco del teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**WM \_ KEYUP.**](wm-keyup.md) **WM \_ DEADCHAR** especifica un código de caracteres generado por una tecla fallida. Una tecla fallido es una clave que genera un carácter, como el umlaut (doble punto), que se combina con otro carácter para formar un carácter compuesto. Por ejemplo, el carácter umlaut-O ( ) se genera escribiendo la tecla fallida para el carácter umlaut y, a continuación, escribiendo la tecla O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter generado por la tecla no generada.

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que la pulsación de tecla se carga de forma automática como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficientemente larga, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo. |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Reservado; no se usan.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si la tecla ALT se mantiene presionada mientras se presiona la tecla . De lo contrario, el valor es 0.                                                                                                                                                     |
| 30    | Estado de la clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.                                                                                                                                                    |
| 31    | Estado de transición. El valor es 1 si se va a liberar la tecla o es 0 si se presiona la tecla .                                                                                                                                                            |

Para obtener más información, vea [Marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Las aplicaciones suelen usar el mensaje **\_ DEADCHAR** de WM para proporcionar al usuario comentarios sobre cada tecla presionada. Por ejemplo, una aplicación puede mostrar el acento en la posición del carácter actual sin mover el carácter de diálogo.

Dado que no hay necesariamente una correspondencia uno a uno entre las teclas presionadas y los mensajes de caracteres generados, la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje [**WM \_ KEYDOWN**](wm-keydown.md) más reciente que precede a la publicación del **mensaje \_ DEADCHAR de WM.**

Para los teclados mejorados de 101 y 102 teclas, las teclas extendidas son la tecla ALT derecha y las teclas CTRL derechas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow en los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Algunos otros teclados pueden admitir el bit de tecla extendida en el *parámetro lParam.*

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

