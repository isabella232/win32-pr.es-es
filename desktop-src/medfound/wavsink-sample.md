---
description: Ejemplo de WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Ejemplo de WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696859"
---
# <a name="wavsink-sample"></a>Ejemplo de WavSink

Muestra cómo implementar un receptor de multimedia personalizado en Microsoft Media Foundation. En el ejemplo se implementa un receptor de archivo que escribe audio PCM sin comprimir en un archivo. wav.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Uso

El ejemplo WavSink contiene dos proyectos de Visual Studio:

-   WavSink. vcproj crea una biblioteca estática que contiene la implementación del receptor de medios.
-   WriteWavFile. vcproj crea una aplicación de consola que usa el receptor de medios para generar un archivo. wav. Esta aplicación se vincula a la biblioteca creada por el proyecto WavSink.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Receptores de medios](media-sinks.md)
</dt> </dl>

 

 



