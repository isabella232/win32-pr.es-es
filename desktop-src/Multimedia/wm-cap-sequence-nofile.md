---
title: WM_CAP_SEQUENCE_NOFILE mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ SEQUENCE \_ NOFILE inicia la captura de vídeo de streaming sin escribir datos en un archivo. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9344b53a52caa2e536483a339439a6d942ff1fea0313767d0e1be520c09b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940733"
---
# <a name="wm_cap_sequence_nofile-message"></a>Mensaje \_ WM CAP SEQUENCE \_ \_ NOFILE

El **mensaje WM CAP SEQUENCE \_ \_ \_ NOFILE** inicia la captura de vídeo de streaming sin escribir datos en un archivo. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSequenceNoFile.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile)


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Comentarios

Este mensaje es útil junto con las funciones de devolución de llamada de secuencia de vídeo o de secuencia de audio de forma de onda que permiten a la aplicación usar los datos de vídeo y audio directamente.

Si desea modificar los parámetros que controlan la captura de streaming, use el mensaje [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) antes de iniciar la captura.

De forma predeterminada, la ventana de captura no permite que otras aplicaciones sigan ejecutándose durante la captura. Para invalidar esto, establezca el miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en **TRUE** o instale una función de devolución de llamada yield.

Durante la captura de streaming, la ventana de captura puede, opcionalmente, emitir notificaciones a la aplicación de tipos específicos de condiciones. Para instalar procedimientos de devolución de llamada para estas notificaciones, use los mensajes siguientes:

-   [**ERROR DE \_ DEVOLUCIÓN \_ DE LLAMADA DEL CONJUNTO \_ DE LÍMITES DE \_ WM**](wm-cap-set-callback-error.md)
-   [**ESTADO DE \_ DEVOLUCIÓN \_ DE LLAMADA DEL CONJUNTO \_ DE LÍMITES DE \_ WM**](wm-cap-set-callback-status.md)
-   [**RENDIMIENTO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





