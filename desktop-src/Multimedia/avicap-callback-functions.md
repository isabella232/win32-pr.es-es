---
title: Funciones de devolución de llamada AVICap
description: Funciones de devolución de llamada AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Clase AVICap, funciones de devolución de llamada
- Funciones de devolución de llamada AVICap, acerca de
- Mensaje WM_CAP_SET_CALLBACK_CAPCONTROL
- Mensaje WM_CAP_SET_CALLBACK_ERROR
- Mensaje WM_CAP_SET_CALLBACK_FRAME
- Mensaje WM_CAP_SET_CALLBACK_STATUS
- Mensaje WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Mensaje WM_CAP_SET_CALLBACK_WAVESTREAM
- Mensaje WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl (macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame (macro)
- capSetCallbackOnStatus (macro)
- capSetCallbackOnVideoStream (macro)
- capSetCallbackOnWaveStream (macro)
- capSetCallbackOnYield (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994561"
---
# <a name="avicap-callback-functions"></a>Funciones de devolución de llamada AVICap

La aplicación puede registrar funciones de devolución de llamada con una ventana de captura para notificar a la aplicación cuando cambia el estado, cuando se produce un error, cuando los búferes de audio y fotogramas de vídeo están disponibles y para obtener resultados durante la captura de streaming. Los siguientes mensajes establecen la función de devolución de llamada.



| Message                                                                        | Descripción                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**devolución de llamada de conjunto de Cap de WM \_ \_ \_ \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Especifica la función de devolución de llamada en la aplicación a la que se llama para proporcionar un control preciso sobre el inicio y el final de la captura. También puede usar la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) para enviar este mensaje.                   |
| [**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-error.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se produce un error. También puede usar la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) para enviar este mensaje.                                                           |
| [**\_marco de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-frame.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se capturan los marcos de vista previa. También puede usar la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) para enviar este mensaje.                                               |
| [**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-status.md)           | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando cambia el estado. También puede usar la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) para enviar este mensaje.                                                      |
| [**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-videostream.md) | Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando hay disponible un nuevo búfer de vídeo. También puede usar la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) para enviar este mensaje. |
| [**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**](wm-cap-set-callback-wavestream.md)   | Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando un nuevo búfer de audio está disponible. También puede usar la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) para enviar este mensaje.   |
| [**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**](wm-cap-set-callback-yield.md)             | Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se produce durante la captura de streaming. También puede usar la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) para enviar este mensaje.                                         |



 

En los temas siguientes se describen las distintas funciones de devolución de llamada, las notificaciones enviadas a las funciones y sus usos.

 

 




