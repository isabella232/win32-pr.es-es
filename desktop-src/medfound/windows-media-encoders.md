---
description: Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación. Para convertir archivos multimedia en formato ASF, puede usar los códecs de audio y vídeo de Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificadores de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697926"
---
# <a name="windows-media-encoders"></a>Codificadores de Windows Media

Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación. Para convertir archivos multimedia en formato ASF, puede usar los códecs de audio y vídeo de Windows Media.

Un codificador se identifica mediante el GUID que representa la categoría: audio o vídeo. El tipo de salida del codificador se representa con el GUID principal y el subtipo del tipo de archivo multimedia.

-   Códecs de audio de Windows Media

    Categoría: **\_ categoría MFT \_ , \_ codificador de audio**

    Tipo principal: MFMediaType \_ audio

    SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Códecs de vídeo de Windows Media

    Categoría: **categoría de MFT \_ \_ \_ codificador de vídeo**

    Tipo principal: vídeo de MFMediaType \_

    SubType: MFVideoFormat \_ Wvc1, MFVideoFormat \_ Wmv3, MFVideoFormat wmv2 \_ , MFVideoFormat \_ WMV1

Estos codificadores se implementan como [Media Foundation Transform](media-foundation-transforms.md) (MFT) y Media Foundation proporcionan acceso a la aplicación a través de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificador. Si utiliza componentes de capa de canalización para la codificación ASF, la MFT del codificador se inserta en la canalización como nodo de transformación, ya que es responsable de transformar los datos multimedia que fluyen a través del origen al receptor. Si el origen es un tipo comprimido, la canalización agrega los descodificadores necesarios para convertir el origen en un tipo sin comprimir. Un codificador tiene un flujo de entrada y un flujo de salida. El codificador recibe datos de entrada y genera datos codificados de acuerdo con la configuración y el formato establecidos por la aplicación antes de la sesión de codificación. El formato del flujo de salida se describe mediante un tipo de medio.

Esta sección contiene los temas siguientes.



| Tema                                                                              | Descripción                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)                  | Explica cómo crear el codificador.                                                         |
| [Propiedades de codificación](configuring-the-encoder.md)                                 | Explica cómo configurar el codificador mediante el establecimiento de las propiedades adecuadas en la MFT del codificador. |
| [Negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md) | Explica cómo establecer los tipos de medios de entrada y salida en el codificador.                            |
| [Configuración de un codificador WMV](configuring-a-wmv-encoder.md)                         | Explica cómo configurar un codificador Windows Media Video (WMV).                              |
| [Establecer un tipo de salida para un codificador WMA](configuring-a-wma-encoder.md)          | Explica cómo establecer un tipo de salida en un codificador Windows Media Audio (WMA).                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



