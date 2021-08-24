---
title: WM_TOUCH mensaje (Winuser.h)
description: Notifica a la ventana cuando uno o varios puntos táctiles, como un dedo o un lápiz, tocan una superficie de digitalizador táctil.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH mensaje Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810105"
---
# <a name="wm_touch-message"></a>Mensaje \_ WM TOUCH

Notifica a la ventana cuando uno o varios puntos táctiles, como un dedo o un lápiz, tocan una superficie de digitalizador táctil.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo contiene el número de puntos táctiles asociados a este mensaje. La palabra de orden superior está reservada para su uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un identificador de entrada táctil que se puede usar en una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) para recuperar información detallada sobre los puntos táctiles asociados a este mensaje.

Este identificador solo es válido dentro del proceso actual y no debe pasarse entre procesos excepto como **LPARAM** en una **llamada SendMessage** o **PostMessage.**

Cuando la aplicación ya no requiere este identificador, la aplicación debe llamar a **CloseTouchInputHandle para** liberar la memoria de proceso asociada a este identificador. Si no lo hace, puede producirse una pérdida de memoria de la aplicación.

Tenga en cuenta que el identificador de entrada táctil de este parámetro ya no es válido después de pasar el mensaje [a DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). [DefWindowProc cerrará](/windows/win32/api/winuser/nf-winuser-defwindowproca) e invalidará este identificador.

Tenga en cuenta también que el identificador de entrada táctil de este parámetro ya no es válido después de que el mensaje se haya reenviado mediante [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una de sus variantes. Estas funciones cerrarán e invalidarán este identificador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa el mensaje, debe llamar a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Si no lo hace, la aplicación pierde memoria porque el identificador de entrada táctil no está cerrado y no se libera la memoria de proceso asociada.

## <a name="remarks"></a>Comentarios

**WM \_ Los** mensajes TOUCH no respetan **las regiones HTTRANSPARENT** de las ventanas. Si una ventana devuelve **HTTRANSPARENT en** respuesta a un mensaje **WM \_ NCHITTEST,** los mensajes del mouse van al elemento primario y los **mensajes WM \_ TOUCH** van directamente a la ventana.

## <a name="examples"></a>Ejemplos

El código siguiente es un ejemplo de cómo obtener información de entrada táctil detallada asociada a este mensaje.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

[Guía de programación de manipulaciones e inercia](manipulation-and-inertia.md)
</dt> <dt>

[Windows Guía de programación de entrada táctil](guide-multi-touch-input.md)
</dt> </dl>

 

