---
description: Los códecs de Windows Media Audio y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Códecs de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697978"
---
# <a name="windows-media-codecs"></a>Códecs de Windows Media

Los códecs de Windows Media Audio y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales. Cada códec consta de dos objetos, un codificador y un descodificador. En esta parte de la documentación se describe cómo usar las características de los códecs de Windows Media Audio y vídeo para generar y consumir flujos de datos comprimidos.

> [!Note]  
> Esta documentación está dirigida principalmente a los desarrolladores que quieren usar códecs de Windows Media en sus aplicaciones multimedia basadas en C++. Para obtener información general técnica de las características de los códecs de Windows Media, consulte [acerca de los códecs de Windows Media](about-the-windows-media-codecs.md).

 

El término *codec* es una fusión de los términos compresor y descompresor. Normalmente, un códec se implementa como un par de objetos COM: uno para codificar el contenido y otro para descodificar el contenido. En algunos casos, los objetos COM ocupan la misma biblioteca vinculada dinámicamente (DLL).

Cada objeto codec implementa dos interfaces independientes pero similares:



| Interfaz                              | Descripción                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible con DirectShow.                 |



 

No solo hay códecs diferentes para audio y vídeo, sino también distintos códecs para diferentes tipos de contenido que puede incluir en un archivo de audio o de vídeo. Los algoritmos que se usan para comprimir y descomprimir datos de palabras pronunciadas difieren de los algoritmos usados para comprimir y descomprimir los datos de música.

## <a name="codec-descriptions"></a>Descripciones de códecs

En la tabla siguiente se describen los usos previstos de los códecs de Windows Media.



| Códec                                                                     | Descripción                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Un códec de audio que admite tres categorías de contenido codificado: estándar, profesional y sin pérdida de información.                                                                                                                                                                                      |
| [Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)            | Códec de audio optimizado para codificar las proporciones de la voz humana a alta compresión. Este es el códec preferido para las secuencias que se componen principalmente de palabras pronunciadas. En el caso de contenido que está mezclado con música y voz, este códec puede cambiar dinámicamente el algoritmo de codificación utilizado para obtener una calidad óptima. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Un códec de vídeo que admite cuatro categorías de contenido codificado: perfil simple, perfil principal, perfil avanzado e imagen.                                                                                                                                                                  |
| [Pantalla de Windows Media Video 9](usingthewindowsmediavideo9screencodec.md) | Códec de vídeo optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos. Este códec se usa a menudo para aprendizaje o soporte técnico de software mediante la grabación de imágenes de supervisión mientras se usan las aplicaciones para equipos.                                                                         |



 

Las versiones más recientes de los objetos codec también habilitan el acceso a algunos códecs heredados, como Windows Media Video 7 y 8, Windows Media screen 7, los códecs MPEG-4 de Microsoft anteriores y los códecs ISO MPEG-4 de Microsoft.

> [!Note]  
> En esta documentación no se tratan estos códecs heredados; solo incluye las versiones actuales de los códecs.

 

En el caso de los códecs anteriores, utilice los mismos procedimientos que al usar los códecs actuales; sin embargo, recuerde que no todas las características se admiten en todos los códecs.

## <a name="in-this-section"></a>En esta sección

-   [Acerca de los códecs de Windows Media](about-the-windows-media-codecs.md)
-   [Usar el códec y los objetos DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Métodos de codificación](encodingmethods.md)
-   [Implementación de códecs](codecimplementation.md)
-   [El modelo de búfer de depósito con fugas](the-leaky-bucket-buffer-model.md)
-   [Trabajar con códec DMOs](workingwithcodecdmos.md)
-   [Trabajar con códec MFTs](workingwithcodecmfts.md)
-   [Trabajar con audio](workingwithaudio.md)
-   [Trabajar con vídeo](workingwithvideo.md)
-   [Almacenar medios comprimidos en archivos AVI](storingcompressedmediainavifiles.md)
-   [Usar la codificación VBR](usingvbrencoding.md)
-   [Uso de la codificación de Two-Pass](usingtwoencodingpasses.md)
-   [Obtener estadísticas de codificación](gettingencodingstatistics.md)
-   [Uso de extensiones de unidad de datos](usingdataunitextensions.md)
-   [Constantes IPropertyBag de códec y DSP](codecanddspproperties.md)
-   [Analizador de tabla de contenido](toc-parser.md)
-   [Preguntas más frecuentes sobre códecs de Windows Media](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
