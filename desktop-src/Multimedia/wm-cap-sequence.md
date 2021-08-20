---
title: WM_CAP_SEQUENCE mensaje (Vfw.h)
description: El mensaje WM \_ CAP SEQUENCE inicia la captura de vídeo y audio de streaming a un \_ archivo. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023fd22d79fdfcd1df1f44b2862814ed809fd93c43ab9cd7122414ee1e27db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800270"
---
# <a name="wm_cap_sequence-message"></a>Mensaje \_ DE SECUENCIA DE WM CAP \_

El **mensaje WM CAP \_ \_ SEQUENCE** inicia la captura de vídeo y audio de streaming a un archivo. Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSequence.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence)


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Comentarios

Si desea modificar los parámetros que controlan la captura de streaming, use el mensaje [**SET \_ SEQUENCE \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) de WM CAP antes de iniciar la captura.

De forma predeterminada, la ventana de captura no permite que otras aplicaciones sigan ejecutándose durante la captura. Para invalidar esto, establezca el miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en **TRUE** o instale una función de devolución de llamada yield.

Durante la captura de streaming, la ventana de captura puede, opcionalmente, emitir notificaciones a la aplicación de tipos específicos de condiciones. Para instalar procedimientos de devolución de llamada para estas notificaciones, use los mensajes siguientes:

-   [**ERROR DE \_ DEVOLUCIÓN \_ DE LLAMADA DEL CONJUNTO \_ DE LÍMITES DE \_ WM**](wm-cap-set-callback-error.md)
-   [**ESTADO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-status.md)
-   [**RENDIMIENTO DE \_ DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





