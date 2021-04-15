---
title: Mensaje de WM_UNICHAR (Winuser. h)
description: '\_Una aplicación puede utilizar el mensaje UNIchar de WM para publicar la entrada en otras ventanas.'
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Entrada de mouse y teclado de mensaje de WM_UNICHAR
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695938"
---
# <a name="wm_unichar-message"></a>Message de WM \_ UNIchar

Una aplicación puede utilizar el mensaje **\_ UNICHAR de WM** para publicar la entrada en otras ventanas. Este mensaje contiene el código de carácter de la tecla que se presionó. (Compruebe si una aplicación de destino puede procesar mensajes de **WM \_ UNICHAR** enviando el mensaje con *wParam* establecido en **Unicode \_ nochar**).


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter de la clave.

Si *wParam* es **Unicode \_ nochar** y la aplicación procesa este mensaje, devuelve **true**. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devolverá **false** (el valor predeterminado).

Si *wParam* no es **Unicode \_**, devuelve **false**. El  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) de Unicode envía un mensaje de [**\_ carácter de WM**](wm-char.md) con los mismos parámetros y la función ANSI **DefWindowProc** envía uno o dos mensajes de **WM \_ Char** con los caracteres ANSI correspondientes.

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

El mensaje de **WM \_ UNICHAR** es similar a [**WM \_ Char**](wm-char.md), pero usa el formato de transformación unicode (UTF)-32, mientras que **WM \_ Char** usa UTF-16.

Este mensaje está diseñado para enviar o exponer caracteres Unicode en ventanas ANSI y puede controlar los caracteres de plano complementario Unicode.

Dado que no hay necesariamente una correspondencia uno a uno entre las claves presionadas y los mensajes de caracteres generados, la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) más reciente que precede a la publicación del mensaje de **WM \_ UNICHAR** .

Para los teclados mejorados de clave 101-y 102, las teclas extendidas son la ALT derecha y las teclas CTRL derecha en la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**carácter de WM \_**](wm-char.md)
</dt> <dt>

[**KEYDOWN de WM \_**](wm-keydown.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

