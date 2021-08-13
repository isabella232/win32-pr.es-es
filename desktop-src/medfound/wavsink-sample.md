---
description: Ejemplo de WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Ejemplo de WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1bd754e426d848e9d84aea337225ea51940d8727c63d1e1c78c93aeea43110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737140"
---
# <a name="wavsink-sample"></a>Ejemplo de WavSink

Muestra cómo implementar un receptor de medios personalizado en Microsoft Media Foundation. El ejemplo implementa un receptor de archivo que escribe audio PCM sin comprimir en un archivo .wav.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las interfaces Media Foundation siguientes:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Uso

El ejemplo WavSink contiene dos proyectos Visual Studio proyecto:

-   WavSink.vcproj compila una biblioteca estática que contiene la implementación del receptor multimedia.
-   WriteWavFile.vcproj compila una aplicación de consola que usa el receptor multimedia para generar un archivo .wav. Esta aplicación se vincula a la biblioteca creada por el proyecto WavSink.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> </dl>

 

 



