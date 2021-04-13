---
title: Mensaje de WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: El \_ \_ \_ \_ mensaje de Videostream de devolución de llamada de devoluciones de Cap de WM establece una función de devolución de llamada en la aplicación.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_VIDEOSTREAM de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421945"
---
# <a name="wm_cap_set_callback_videostream-message"></a>\_Mensaje de \_ \_ Videostream de devolución de llamada de Cap de WM \_

El mensaje de **\_ \_ \_ \_ Videostream de devolución de llamada de devoluciones de Cap de WM** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento durante la captura de streaming cuando se rellena un búfer de vídeo. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de flujo de vídeo, de tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de flujo de vídeo instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

La ventana captura llama a la función de devolución de llamada antes de escribir el fotograma capturado en el disco. Esto permite que las aplicaciones modifiquen el marco si se desea.

Si se usa una función de devolución de llamada de secuencia de vídeo para la captura de streaming, el procedimiento debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitado mientras dure la sesión. Se puede deshabilitar después de que finalice la captura de streaming.

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

 

 





