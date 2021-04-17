---
title: Mensaje de WM_KEYDOWN (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando se presiona una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Entrada de mouse y teclado de mensaje de WM_KEYDOWN
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
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700251"
---
# <a name="wm_keydown-message"></a>\_Mensaje KEYDOWN de WM

Se envía a la ventana con el foco de teclado cuando se presiona una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de tecla virtual de la clave que no es del sistema. Consulte [códigos de tecla virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra a continuación.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Número de repeticiones del mensaje actual. El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla. Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes. Sin embargo, el número de repeticiones no es acumulativo. |
| 16-23 | Código de recorrido. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Sector No use.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor siempre es 0 para un mensaje de **\_ KEYDOWN de WM** .                                                                                                                                                                                                |
| 30    | Estado de la clave anterior. El valor es 1 si la tecla está inactiva antes de que se envíe el mensaje o es cero si la clave está activa.                                                                                                                                                 |
| 31    | Estado de transición. El valor siempre es 0 para un mensaje de **\_ KEYDOWN de WM** .                                                                                                                                                                                            |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).
 

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

Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) en github.


## <a name="remarks"></a>Observaciones

Si se presiona la tecla F10, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece una marca interna. Cuando **DefWindowProc** recibe el mensaje de [**\_ KEYUP de WM**](wm-keyup.md) , la función comprueba si se ha establecido la marca interna y, en caso afirmativo, envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior. El parámetro **WM \_ SYSCOMMAND** del mensaje se establece en SC \_ KEYMENU.

Debido a la característica de repetición de la función, se puede publicar más de un mensaje de **\_ KEYDOWN de WM** antes de que se exponga un mensaje de [**\_ KEYUP de WM**](wm-keyup.md) . El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje de **\_ KEYDOWN de WM** indica la primera transición o una transición hacia abajo.

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

[**carácter de WM \_**](wm-char.md)
</dt> <dt>

[**KEYUP de WM \_**](wm-keyup.md)
</dt> <dt>

[**SYSCOMMAND de WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

