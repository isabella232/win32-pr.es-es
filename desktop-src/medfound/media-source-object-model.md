---
description: Modelo de objetos de origen de medios
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modelo de objetos de origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361905"
---
# <a name="media-source-object-model"></a>Modelo de objetos de origen de medios

En este tema se describe el modelo de objetos para orígenes multimedia en Microsoft Media Foundation. Un origen multimedia debe implementar dos objetos:

-   Descriptor de presentación, que describe el contenido del origen, incluido el número de flujos y el formato de cada flujo. Para obtener más información acerca de los descriptores de presentación, vea [descriptores de presentación](presentation-descriptors.md).
-   Uno o más flujos multimedia, que generan los datos de origen.

El origen no crea los flujos hasta que se inicia la reproducción.

## <a name="media-source-interfaces"></a>Interfaces de origen multimedia

Un origen multimedia debe exponer las siguientes interfaces a través de **QueryInterface**.



| Interfaz                                                | Descripción                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Se requiere para todos los orígenes multimedia.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Se requiere para todos los orígenes multimedia. La interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) hereda esta interfaz. |



 

Opcionalmente, un origen multimedia puede implementar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementar cualquiera de las siguientes interfaces como servicios:



| Interfaz de servicio                                  | Descripción                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | Controla la velocidad de reproducción.                                       |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | Indica el intervalo de velocidades de reproducción que se admiten.           |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | Permite que el administrador de calidad ajuste la calidad de audio o vídeo. |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | Proporciona metadatos.                                                |



 

Si el origen de medios se puede reproducir a velocidades distintas de la velocidad normal (1,0), debe exponer el servicio de control de velocidad ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) y [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)). De lo contrario, se supone que el origen solo admite la reproducción a velocidad normal. Para obtener más información, vea [implementar el control de tasa](implementing-rate-control.md).

Para obtener más información sobre las interfaces de servicio y [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de servicio](service-interfaces.md).

## <a name="media-stream-interfaces"></a>Interfaces de flujo multimedia

Los flujos multimedia deben implementar las siguientes interfaces.



| Interfaz                                                | Descripción                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | Se requiere para todos los flujos multimedia.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Se requiere para todos los flujos multimedia. La interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) hereda esta interfaz. |



 

Actualmente no hay interfaces de servicio definidas para flujos multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> </dl>

 

 



