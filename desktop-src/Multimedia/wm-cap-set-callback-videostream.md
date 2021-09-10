---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM mensaje (Vfw.h)
description: El mensaje \_ VIDEOSTREAM DE DEVOLUCIÓN DE LLAMADA DE WM CAP SET \_ establece una función \_ de \_ devolución de llamada en la aplicación.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371492"
---
# <a name="wm_cap_set_callback_videostream-message"></a>Mensaje \_ \_ VIDEOSTREAM DE \_ DEVOLUCIÓN DE LLAMADA DE \_ WM CAP SET

El **mensaje \_ VIDEOSTREAM DE \_ \_ DEVOLUCIÓN DE LLAMADA \_** DE WM CAP SET establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento durante la captura de streaming cuando se rellena un búfer de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnVideoStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream)


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada video-stream, de tipo [**capVideoStreamCallback.**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback) Especifique **NULL** para este parámetro para deshabilitar una función de devolución de llamada de secuencia de vídeo instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **si** la captura de streaming o una sesión de captura de un solo fotograma están en curso.

## <a name="remarks"></a>Observaciones

La ventana de captura llama a la función de devolución de llamada antes de escribir el fotograma capturado en el disco. Esto permite a las aplicaciones modificar el marco si lo desea.

Si se usa una función de devolución de llamada de secuencia de vídeo para la captura de streaming, el procedimiento debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitado mientras dure la sesión. Se puede deshabilitar una vez que finaliza la captura de streaming.

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

 

 





