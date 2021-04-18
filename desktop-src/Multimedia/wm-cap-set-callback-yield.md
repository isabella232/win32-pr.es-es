---
title: Mensaje de WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: El \_ \_ \_ mensaje de Yield devoluciones de llamada del límite \_ de WM establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura produce durante la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_YIELD de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676567"
---
# <a name="wm_cap_set_callback_yield-message"></a>\_Mensaje de \_ \_ yield devoluciones de llamada de Cap de WM \_

El mensaje de **\_ \_ \_ \_ yield devoluciones de llamada del límite de WM** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura produce durante la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada Yield, de tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada yield instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada yield. Se llama a la función de devolución de llamada yield al menos una vez para cada fotograma de vídeo capturado durante la captura de streaming. Si se instala una función de devolución de llamada Yield, se llamará independientemente del estado del miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

Si se usa la función de devolución de llamada Yield, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión. Se puede deshabilitar después de que finalice la captura de streaming.

Normalmente, las aplicaciones realizan algún tipo de procesamiento de mensajes en la función de devolución de llamada que consta de un bucle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , como en el bucle de mensajes de una función [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) . La función de devolución de llamada yield también debe filtrar y quitar los mensajes que pueden provocar problemas de reentrada.

Normalmente, una aplicación devuelve **true** en el procedimiento Yield para continuar con la captura de streaming. Si una función de devolución de llamada yield devuelve **false**, la ventana de captura detiene el proceso de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

