---
title: WM_UNICHAR mensaje (Winuser.h)
description: Una aplicación puede usar el mensaje \_ WM UNICHAR para publicar entradas en otras ventanas.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR entrada de teclado y mouse
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241562"
---
# <a name="wm_unichar-message"></a>Mensaje \_ DE WM UNICHAR

Una aplicación puede usar el mensaje **\_ WM UNICHAR** para publicar entradas en otras ventanas. Este mensaje contiene el código de carácter de la tecla que se presionó. (Pruebe si una aplicación de destino puede procesar **mensajes \_ WM UNICHAR** enviando el mensaje con *wParam* establecido en **UNICODE \_ NOCHAR).**


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter de la clave.

Si *wParam* es **UNICODE \_ NOCHAR y** la aplicación procesa este mensaje, devuelva **TRUE**. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devolverá **FALSE** (valor predeterminado).

Si *wParam* no es **UNICODE \_ NOCHAR,** devuelva **FALSE.** Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) publica un mensaje [**\_ WM CHAR**](wm-char.md) con los mismos parámetros y la función ANSI **DefWindowProc** publica uno o dos mensajes **WM \_ CHAR** con los caracteres ANSI correspondientes.

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
| 29    | Código de contexto. El valor es 1 si la tecla ALT se mantiene presionada mientras se presiona la tecla . De lo contrario, el valor es 0.                                                                                                                                                     |
| 30    | Estado de clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.                                                                                                                                                    |
| 31    | Estado de transición. El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.                                                                                                                                                            |

Para obtener más información, vea [Marcas de mensaje de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

El **mensaje \_ UNICHAR de WM** es similar a WM [**\_ CHAR,**](wm-char.md)pero usa el formato de transformación Unicode (UTF)-32, mientras que **WM \_ CHAR** usa UTF-16.

Este mensaje está diseñado para enviar o publicar caracteres Unicode en ventanas ANSI y puede controlar caracteres de plano complementario Unicode.

Dado que no hay necesariamente una correspondencia uno a uno entre las teclas presionadas y los mensajes de caracteres generados, la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje [**\_ WM KEYDOWN**](wm-keydown.md) más reciente que precede a la publicación del **mensaje \_ UNICHAR de WM.**

En el caso de los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT derecha y CTRL derechas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow de los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Algunos otros teclados pueden admitir el bit de clave extendida en el *parámetro lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ CHAR**](wm-char.md)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

