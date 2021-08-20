---
title: Clase MediaRenderer
description: Implementa la interfaz IMediaRenderer que representa un dispositivo DLNA Digital Media Renderer (DMR).
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- MediaRenderer class Media Streaming API
- MediaRenderer class Media Streaming API , descrito
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b003c0c24838b77e044fc0bf14beaac0c97eeebd64415d74ca77bd2e8a44a105
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870832"
---
# <a name="mediarenderer-class"></a>Clase MediaRenderer

Implementa la interfaz [**IMediaRenderer que**](imediarenderer.md) representa un dispositivo DLNA Digital Media Renderer (DMR).

**MediaRenderer** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MediaRenderer** tiene estos métodos.



| Método                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Registra un controlador de eventos para el [**evento RenderingParametersUpdate.**](renderingparametersupdate.md)<br/>                                                                                                                                                                                                                                                       |
| [**add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Registra un controlador de eventos para el [**evento TransportParametersUpdate.**](transportparametersupdate.md)<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Consulta la DMR de forma asincrónica para determinar si el audio está actualmente muted o unmuted.<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Consulta la DMR de forma asincrónica para recuperar información de posición.<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Consulta la DMR de forma asincrónica para recuperar información de transporte.<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Consulta la DMR de forma asincrónica para su nivel de volumen de audio actual.<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | Indica a la DMR de forma asincrónica que pause la reproducción del contenido actual.<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Indica a la DMR de forma asincrónica que reprodúe el contenido especificado mediante una llamada al método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync.**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Indica a la DMR de forma asincrónica que reprodúe el contenido especificado mediante una llamada al método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) a la velocidad especificada.<br/> |
| [**remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Anula el registro de un controlador de eventos para el [**evento RenderingParametersUpdate.**](renderingparametersupdate.md)<br/>                                                                                                                                                                                                                                                     |
| [**remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Anula el registro de un controlador de eventos para el [**evento TransportParametersUpdate.**](transportparametersupdate.md)<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Indica a la DMR de forma asincrónica que busque un desplazamiento de tiempo determinado.<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Indica a la DMR de forma asincrónica que silencie o desmuescie el audio.<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Indica a la DMR de forma asincrónica que prepare el contenido especificado para reproducirlo una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Indica a la DMR de forma asincrónica que prepare la secuencia multimedia especificada para reproducirla una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Indica a la DMR de forma asincrónica que prepare el contenido identificado por el URI especificado para reproducirlo una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Indica a la DMR de forma asincrónica que prepare el contenido especificado para la reproducción.<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Indica a la DMR de forma asincrónica que prepare la secuencia multimedia especificada para reproducirla una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Indica a la DMR de forma asincrónica que prepare el contenido identificado por el URI especificado para la reproducción.<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Establece el nivel de volumen de audio de la DMR de forma asincrónica en el valor especificado.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Indica a la DMR de forma asincrónica que deje de reproducir el contenido actual.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Propiedades

La **clase MediaRenderer** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**ActionInformation**](mediarenderer-actioninformation.md)<br/> | Solo lectura<br/> | Obtiene información sobre qué métodos se pueden invocar actualmente en la DMR.<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si la DMR es capaz de reproducir contenido de audio.<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si la DMR es capaz de mostrar imágenes.<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si la DMR es capaz de reproducir contenido de vídeo.<br/> |



 

 

