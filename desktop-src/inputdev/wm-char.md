---
title: Mensaje de WM_CHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje KEYDOWN de WM. El \_ mensaje de caracteres de WM contiene el código de carácter de la tecla que se presionó.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Entrada de mouse y teclado de mensaje de WM_CHAR
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
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718767"
---
# <a name="wm_char-message"></a>Mensaje de carácter de WM \_

Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**\_ KEYDOWN de WM**](wm-keydown.md) . El mensaje de caracteres de **WM \_** contiene el código de carácter de la tecla que se presionó.


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
Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) en github.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ carácter de WM** usa el formato de transformación Unicode (UTF)-16.

No hay necesariamente una correspondencia uno a uno entre las claves presionadas y los mensajes de caracteres generados, por lo que la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones. La información de la palabra de orden superior solo se aplica al mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) más reciente que precede a la publicación del mensaje de **\_ carácter de WM** .

Para los teclados mejorados de clave 101-y 102, las teclas extendidas son la ALT derecha y las teclas CTRL derecha en la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

El mensaje de conversión [**\_ UNICHAR de WM**](wm-unichar.md) es el mismo que el de **WM \_ Char**, salvo que usa UTF-32. Está diseñado para enviar o exponer caracteres Unicode en ventanas ANSI y puede controlar los caracteres de plano complementario Unicode.

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

[**UNICHAR de WM \_**](wm-unichar.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

