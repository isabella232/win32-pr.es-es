---
title: Clase MediaRenderer
description: Implementa la interfaz IMediaRenderer que representa un dispositivo de representador de medios digitales DLNA (DMR).
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- Clase MediaRenderer API de streaming de multimedia
- Clase MediaRenderer API de streaming de multimedia, descrita
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d14cdea89535fc680874905a9fb2b3358595baab
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533124"
---
# <a name="mediarenderer-class"></a>Clase MediaRenderer

Implementa la interfaz [**IMediaRenderer**](imediarenderer.md) que representa un dispositivo de representador de medios digitales DLNA (DMR).

**MediaRenderer** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MediaRenderer** tiene estos métodos.



| Método                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**agregar \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Registra un controlador de eventos para el evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**agregar \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Registra un controlador de eventos para el evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Consulta el DMR de forma asincrónica para determinar si el audio está silenciado o no está silenciado.<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Consulta el DMR de forma asincrónica para recuperar la información de posición.<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Consulta el DMR de forma asincrónica para recuperar la información de transporte.<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Consulta el DMR de forma asincrónica para obtener el nivel de volumen de audio actual.<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | Indica al DMR de forma asincrónica que PAUSE la reproducción del contenido actual.<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Indica al DMR de forma asincrónica que reproduzca el contenido que se especificó mediante una llamada al método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) .<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Indica a DMR de forma asincrónica que reproduzca el contenido que se especificó mediante una llamada al método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) a la velocidad especificada.<br/> |
| [**quitar \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Anula el registro de un controlador de eventos para el evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**quitar \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Anula el registro de un controlador de eventos para el evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Indica al DMR de forma asincrónica que busque un desplazamiento de tiempo determinado.<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Indica al DMR de forma asincrónica que silencie o desmute el audio.<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Indica de forma asincrónica a DMR que prepare el contenido especificado para que se reproduzca una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Indica de forma asincrónica a DMR que prepare el flujo multimedia especificado para que se reproduzca una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Indica de forma asincrónica a DMR que prepare el contenido identificado por el URI especificado para reproducirlo una vez que haya terminado de reproducirse el contenido actual.<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Indica de forma asincrónica a los DMR para preparar el contenido especificado para la reproducción.<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Indica de forma asincrónica a DMR que prepare el flujo multimedia especificado para que se reproduzca una vez que el contenido actual haya terminado de reproducirse.<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Indica de forma asincrónica a los DMR para preparar el contenido identificado por el URI especificado para la reproducción.<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Establece el nivel de volumen de audio en el DMR de forma asincrónica en el valor especificado.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Indica al DMR de forma asincrónica que detenga la reproducción del contenido actual.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Propiedades

La clase **MediaRenderer** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**ActionInformation**](mediarenderer-actioninformation.md)<br/> | Solo lectura<br/> | Obtiene información acerca de los métodos que se pueden invocar actualmente en el DMR.<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si el DMR es capaz de reproducir contenido de audio.<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si el DMR es capaz de mostrar imágenes.<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | Solo lectura<br/> | Obtiene un valor que indica si el DMR es capaz de reproducir contenido de vídeo.<br/> |



 

 

