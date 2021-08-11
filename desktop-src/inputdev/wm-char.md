---
title: WM_CHAR mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando la función TranslateMessage traduce un mensaje \_ WM KEYDOWN. El mensaje CHAR de WM \_ contiene el código de carácter de la tecla que se presionó.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 16f9f1160f9766bd6284f62f2203b940ab6336f326aa31a0d9fa2894d243cf59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247954"
---
# <a name="wm_char-message"></a>Mensaje CHAR de WM \_

Se publica en la ventana con el foco del teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**WM \_ KEYDOWN.**](wm-keydown.md) El **mensaje CHAR \_ de WM** contiene el código de carácter de la tecla que se presionó.


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter de la clave.

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

## <a name="example"></a>Ejemplo

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) en GitHub.

## <a name="remarks"></a>Comentarios

El **mensaje CHAR \_ de WM** usa el formato de transformación Unicode (UTF)-16.

No hay necesariamente una correspondencia uno a uno entre las teclas presionadas y los mensajes de caracteres generados, por lo que la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje [**WM \_ KEYDOWN**](wm-keydown.md) más reciente que precede a la publicación del **mensaje CHAR \_ de WM.**

En el caso de los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT derecha y CTRL derechas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow de los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Algunos otros teclados pueden admitir el bit de clave extendida en el *parámetro lParam.*

El [**mensaje \_ UNICHAR de WM**](wm-unichar.md) es el mismo que WM **\_ CHAR,** salvo que usa UTF-32. Está diseñado para enviar o publicar caracteres Unicode en ventanas ANSI y puede controlar caracteres de plano complementario Unicode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ UNICHAR**](wm-unichar.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

