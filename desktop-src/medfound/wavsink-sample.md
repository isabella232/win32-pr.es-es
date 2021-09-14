---
description: Ejemplo wavsink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Ejemplo wavsink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363615"
---
# <a name="wavsink-sample"></a>Ejemplo wavsink

Muestra cómo implementar un receptor multimedia personalizado en Microsoft Media Foundation. El ejemplo implementa un receptor de archivo que escribe audio PCM sin comprimir en un archivo .wav.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes Media Foundation interfaces:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Uso

El ejemplo WavSink contiene dos Visual Studio proyecto:

-   WavSink.vcproj compila una biblioteca estática que contiene la implementación del receptor multimedia.
-   WriteWavFile.vcproj compila una aplicación de consola que usa el receptor multimedia para generar un archivo .wav. Esta aplicación se vincula a la biblioteca creada por el proyecto WavSink.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de GitHub Windows ejemplos clásicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> </dl>

 

 



