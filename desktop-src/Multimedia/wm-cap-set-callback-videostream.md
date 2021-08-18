---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM mensaje (Vfw.h)
description: El mensaje \_ WM CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM establece una función de devolución de llamada en la aplicación.
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
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940723"
---
# <a name="wm_cap_set_callback_videostream-message"></a>Mensaje \_ \_ VIDEOSTREAM DE \_ DEVOLUCIÓN DE LLAMADA DE \_ WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ VIDEOSTREAM** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento durante la captura de streaming cuando se rellena un búfer de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnVideoStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream)


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada video-stream, de tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada de secuencia de vídeo instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE si** la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Comentarios

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

 

 





