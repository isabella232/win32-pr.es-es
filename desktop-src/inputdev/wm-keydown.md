---
title: WM_KEYDOWN mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando se presiona una tecla no del sistema. Una tecla no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9f54d0cad58a378d12247127d1ed70ab48653e18f4cceeb3c801efcf2aaae66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717205"
---
# <a name="wm_keydown-message"></a>Mensaje \_ DE WM KEYDOWN

Se publica en la ventana con el foco del teclado cuando se presiona una tecla no del sistema. Una tecla no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la clave no del sistema. Consulte [Códigos de clave virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Recuento de repeticiones, código de examen, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, como se muestra a continuación.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que se autorpeda la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficientemente larga, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo. |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; De lo contrario, es 0.                                                              |
| 25-28 | Reservado; no se usan.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor siempre es 0 para un **mensaje \_ WM KEYDOWN.**                                                                                                                                                                                                |
| 30    | Estado de clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es cero si la clave está arriba.                                                                                                                                                 |
| 31    | Estado de transición. El valor siempre es 0 para un **mensaje \_ WM KEYDOWN.**                                                                                                                                                                                            |

Para obtener más información, vea [Marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="example"></a>Ejemplo

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) en GitHub.


## <a name="remarks"></a>Comentarios

Si se presiona la tecla F10, la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece una marca interna. Cuando **DefWindowProc** recibe el mensaje [**WM \_ KEYUP,**](wm-keyup.md) la función comprueba si la marca interna está establecida y, si es así, envía un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM a la ventana de nivel superior. El **parámetro \_ WM SYSCOMMAND** del mensaje se establece en SC \_ KEYMENU.

Debido a la característica de autorepeat, se puede publicar más de un mensaje **WM \_ KEYDOWN** antes de que se publique un mensaje [**DE WM \_ KEYUP.**](wm-keyup.md) El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje **WM \_ KEYDOWN** indica la primera transición hacia abajo o una transición hacia abajo repetida.

Para los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT y CTRL correctas en la sección principal del teclado. las teclas de dirección INS, DEL, HOME, END, PAGE UP, PAGE DOWN y en los clústeres situados a la izquierda del teclado numérico. y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de tecla extendida en el *parámetro lParam.*

Las aplicaciones deben *pasar wParam* [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sin modificarlo en absoluto.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ CHAR**](wm-char.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

