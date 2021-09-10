---
title: Funciones de devolución de llamada de AVICap
description: Funciones de devolución de llamada de AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Clase AVICap, funciones de devolución de llamada
- Funciones de devolución de llamada de AVICap, acerca de
- WM_CAP_SET_CALLBACK_CAPCONTROL mensaje
- WM_CAP_SET_CALLBACK_ERROR mensaje
- WM_CAP_SET_CALLBACK_FRAME mensaje
- WM_CAP_SET_CALLBACK_STATUS mensaje
- WM_CAP_SET_CALLBACK_VIDEOSTREAM mensaje
- WM_CAP_SET_CALLBACK_WAVESTREAM mensaje
- WM_CAP_SET_CALLBACK_YIELD mensaje
- CapSetCallbackOnCapControl macro
- capSetCallbackOnErrormacro
- CapSetCallbackOnFrame (macro)
- CapSetCallbackOnStatus (macro)
- CapSetCallbackOnVideoStream macro
- CapSetCallbackOnWaveStream macro
- CapSetCallbackOnYield macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372002"
---
# <a name="avicap-callback-functions"></a>Funciones de devolución de llamada de AVICap

La aplicación puede registrar funciones de devolución de llamada con una ventana de captura para que notifique a la aplicación cuándo cambia el estado, cuándo se producen errores, cuándo están disponibles los búferes de audio y fotogramas de vídeo y para que se produzca durante la captura de streaming. Los mensajes siguientes establecen la función de devolución de llamada.



| Message                                                                        | Descripción                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Especifica la función de devolución de llamada en la aplicación a la que se llama para proporcionar un control preciso sobre el inicio y el final de la captura. También puede usar la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) para enviar este mensaje.                   |
| [**ERROR DE \_ DEVOLUCIÓN \_ DE LLAMADA DEL CONJUNTO \_ DE LÍMITES DE \_ WM**](wm-cap-set-callback-error.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se produce un error. También puede usar la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) para enviar este mensaje.                                                           |
| [**MARCO DE DEVOLUCIÓN DE LLAMADA DE WM \_ CAP \_ SET \_ \_**](wm-cap-set-callback-frame.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se capturan fotogramas de vista previa. También puede usar la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) para enviar este mensaje.                                               |
| [**ESTADO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-status.md)           | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando cambia el estado. También puede usar la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) para enviar este mensaje.                                                      |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md) | Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando hay disponible un nuevo búfer de vídeo. También puede usar la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) para enviar este mensaje. |
| [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)   | Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando hay disponible un nuevo búfer de audio. También puede usar la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) para enviar este mensaje.   |
| [**RENDIMIENTO DE DEVOLUCIÓN DE LLAMADA DEL CONJUNTO DE \_ \_ \_ LÍMITES \_ DE WM**](wm-cap-set-callback-yield.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama al producirse durante la captura de streaming. También puede usar la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) para enviar este mensaje.                                         |



 

En los temas siguientes se describen las diferentes funciones de devolución de llamada, las notificaciones enviadas a las funciones y sus usos.

 

 




