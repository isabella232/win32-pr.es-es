---
description: Los Windows de audio multimedia y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Códecs de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863bb21e17200016317ce273ecb8e2493b9d6bea7d19f92f3f397fb61b88eba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972534"
---
# <a name="windows-media-codecs"></a>Códecs de Windows Media

Los Windows de audio multimedia y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales. Cada códec consta de dos objetos, un codificador y un descodificador. En esta parte de la documentación se describe cómo usar las características de los códecs Windows Media Audio y Video para generar y consumir flujos de datos comprimidos.

> [!Note]  
> Esta documentación está dirigida principalmente a desarrolladores que desean usar códecs Windows media en sus aplicaciones multimedia basadas en C++. Para obtener información general técnica de las características de los códecs Windows media, vea Acerca de [los códecs](about-the-windows-media-codecs.md)Windows multimedia .

 

El término *códec* es una amalgamación de los términos tiempo y descompresión. Normalmente, un códec se implementa como un par de objetos COM: uno para codificar contenido y otro para la codificación de contenido. En algunos casos, los objetos COM ocupan la misma biblioteca vinculada dinámicamente (DLL).

Cada objeto de códec implementa dos interfaces independientes pero similares:



| Interfaz                              | Descripción                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible con DirectShow.                 |



 

No solo hay códecs diferentes para audio y vídeo, sino también códecs diferentes para diferentes tipos de contenido que puede que quiera colocar en un archivo de audio o vídeo. Los algoritmos usados para comprimir y descomprimir datos de palabras habladas difieren de los algoritmos usados para comprimir y descomprimir datos de música.

## <a name="codec-descriptions"></a>Descripciones de códecs

En la tabla siguiente se describen los usos previstos de los códecs Windows media.



| Códec                                                                     | Descripción                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Códec de audio que admite tres categorías de contenido codificado: Standard, Professional y Lossless.                                                                                                                                                                                      |
| [Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)            | Códec de audio optimizado para codificar la voz humana con relaciones de compresión elevadas. Este es el códec preferido para las secuencias que constan principalmente de palabras habladas. En el caso del contenido que mezcla música y voz, este códec puede cambiar dinámicamente el algoritmo de codificación usado para obtener una calidad óptima. |
| [Windows Vídeo multimedia 9](windowsmediavideo9encoder.md)                    | Códec de vídeo que admite cuatro categorías de contenido codificado: Perfil simple, Perfil principal, Perfil avanzado e Imagen.                                                                                                                                                                  |
| [Windows Pantalla vídeo multimedia 9](usingthewindowsmediavideo9screencodec.md) | Códec de vídeo optimizado para codificar capturas de pantalla secuenciales desde monitores de equipo. Este códec se usa a menudo para el entrenamiento o la compatibilidad de software mediante la grabación de imágenes de supervisión mientras se usan aplicaciones de equipo.                                                                         |



 

Las versiones más recientes de los objetos de códec también permiten el acceso a algunos códecs heredados, incluidos Windows Media Video 7 y 8, Windows Media Screen 7, los códecs mpeg-4 de Microsoft antiguos y los códecs MPEG-4 de Microsoft ISO.

> [!Note]  
> En esta documentación no se cubren estos códecs heredados; solo cubre las versiones actuales de códecs.

 

Para los códecs más antiguos, use los mismos procedimientos que al usar los códecs actuales; sin embargo, recuerde que no todas las características se admiten en todos los códecs.

## <a name="in-this-section"></a>En esta sección

-   [Acerca de los códecs Windows multimedia](about-the-windows-media-codecs.md)
-   [Uso del códec y los objetos DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Métodos de codificación](encodingmethods.md)
-   [Implementación de códec](codecimplementation.md)
-   [El modelo de búfer de cubo filtrada](the-leaky-bucket-buffer-model.md)
-   [Trabajar con DDO de códec](workingwithcodecdmos.md)
-   [Trabajar con codec MFT](workingwithcodecmfts.md)
-   [Trabajar con audio](workingwithaudio.md)
-   [Trabajar con vídeo](workingwithvideo.md)
-   [Almacenamiento de medios comprimidos en archivos AVI](storingcompressedmediainavifiles.md)
-   [Uso de la codificación VBR](usingvbrencoding.md)
-   [Uso de Two-Pass codificación](usingtwoencodingpasses.md)
-   [Obtención de estadísticas de codificación](gettingencodingstatistics.md)
-   [Uso de extensiones de unidad de datos](usingdataunitextensions.md)
-   [Constantes IPropertyBag de códec y DSP](codecanddspproperties.md)
-   [Analizador de tabla de contenido](toc-parser.md)
-   [Windows Preguntas más frecuentes sobre códecs multimedia](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
