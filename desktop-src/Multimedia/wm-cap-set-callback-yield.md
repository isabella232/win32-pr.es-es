---
title: WM_CAP_SET_CALLBACK_YIELD mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ SET \_ CALLBACK YIELD establece una función de \_ devolución de llamada en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura se produce durante la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD mensaje Windows Multimedia
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
ms.openlocfilehash: ee12db79a9e4808442618ca295694611aa9e098a87c8f72b25f04360e156c8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622240"
---
# <a name="wm_cap_set_callback_yield-message"></a>Mensaje DE \_ RENDIMIENTO DE \_ \_ DEVOLUCIÓN DE LLAMADA DE \_ WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ YIELD** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento cuando la ventana de captura se produce durante la captura de streaming. Puede enviar este mensaje explícitamente o mediante la [**macro capSetCallbackOnYield.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield)


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada yield, de tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada yield instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE si** la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Opcionalmente, las aplicaciones pueden establecer una función de devolución de llamada yield. La función de devolución de llamada yield se llama al menos una vez para cada fotograma de vídeo capturado durante la captura de streaming. Si se instala una función de devolución de llamada yield, se llamará a ella independientemente del estado del miembro **fYield** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

Si se usa la función de devolución de llamada yield, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión. Se puede deshabilitar una vez que finaliza la captura de streaming.

Las aplicaciones suelen realizar algún tipo de procesamiento de mensajes en la función de devolución de llamada que consta de un bucle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage,](/windows/win32/api/winuser/nf-winuser-translatemessage) [DispatchMessage,](/windows/win32/api/winuser/nf-winuser-dispatchmessage) como en el bucle de mensajes de una [función WinMain.](/windows/win32/api/winbase/nf-winbase-winmain) La función de devolución de llamada yield también debe filtrar y quitar los mensajes que pueden causar problemas de reentrete.

Normalmente, una aplicación devuelve **TRUE en** el procedimiento yield para continuar con la captura de streaming. Si una función de devolución de llamada yield devuelve **FALSE,** la ventana de captura detiene el proceso de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

