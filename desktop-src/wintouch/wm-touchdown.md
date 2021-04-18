---
title: Mensaje de WM_TOUCH (Winuser. h)
description: Notifica a la ventana cuando uno o más puntos táctiles, como un dedo o un lápiz, tocan una superficie del digitalizador sensible al tacto.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- Mensaje de WM_TOUCH de Windows Touch
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
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422452"
---
# <a name="wm_touch-message"></a>\_Mensaje táctil de WM

Notifica a la ventana cuando uno o más puntos táctiles, como un dedo o un lápiz, tocan una superficie del digitalizador sensible al tacto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior contiene el número de puntos de toque asociados a este mensaje. La palabra de orden superior se reserva para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un identificador de entrada táctil que se puede usar en una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) para recuperar información detallada sobre los puntos de toque asociados a este mensaje.

Este identificador solo es válido en el proceso actual y no se debe pasar entre procesos salvo como **lParam** en una llamada **SendMessage** o **PostMessage** .

Cuando la aplicación ya no requiere este identificador, la aplicación debe llamar a **CloseTouchInputHandle** para liberar la memoria de proceso asociada a este identificador. Si no lo hace, puede producirse una pérdida de memoria de la aplicación.

Tenga en cuenta que el identificador de entrada táctil de este parámetro ya no es válido después de que el mensaje se haya pasado a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) cerrará e invalidará este identificador.

Tenga en cuenta también que el identificador de entrada táctil de este parámetro ya no es válido después de que el mensaje se haya reenviado mediante [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una de sus variantes. Estas funciones cerrarán e invalidarán este identificador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa el mensaje, debe llamar a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Si no lo hace, la aplicación perderá memoria porque el identificador de entrada táctil no está cerrado y no se libera la memoria de proceso asociada.

## <a name="remarks"></a>Observaciones

**WM \_ Los mensajes TÁCTILes** no respetan las regiones de **HTTRANSPARENT** de Windows. Si una ventana devuelve **HTTRANSPARENT** en respuesta a un mensaje de **\_ NCHITTEST de WM** , los mensajes del mouse van al elemento primario y los mensajes **\_ táctiles de WM** van directamente a la ventana.

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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

[Guía de programación de manipulaciones e inercia](manipulation-and-inertia.md)
</dt> <dt>

[Guía de programación de entrada táctil de Windows](guide-multi-touch-input.md)
</dt> </dl>

 

