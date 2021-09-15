---
description: Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación. Para convertir archivos multimedia al formato ASF, puede usar los códecs Windows audio y vídeo multimedia.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Codificadores multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468580"
---
# <a name="windows-media-encoders"></a>Windows Codificadores multimedia

Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos en el formato especificado por la aplicación. Para convertir archivos multimedia al formato ASF, puede usar los códecs Windows audio y vídeo multimedia.

Un codificador se identifica mediante el GUID que representa la categoría: audio o vídeo. El tipo de salida del codificador se representa mediante el GUID principal de un tipo de medio y el subtipo.

-   Windows Códecs de audio multimedia

    Categoría: **CODIFICADOR DE AUDIO CATEGORÍA \_ \_ \_ MFT**

    Tipo principal: AUDIO \_ MFMediaType

    SubTipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Códecs de vídeo multimedia

    Categoría: **CODIFICADOR DE VÍDEO DE CATEGORÍA \_ \_ \_ MFT**

    Tipo principal: VÍDEO \_ MFMediaType

    Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Estos codificadores se [](media-foundation-transforms.md) implementan como Media Foundation transformación (MFT) y Media Foundation acceso a la aplicación a través de la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificador. Si usa componentes de capa de canalización para la codificación ASF, el MFT del codificador se inserta en la canalización como un nodo de transformación porque es responsable de transformar los datos multimedia que fluyen a través del origen al receptor. Si el origen es un tipo comprimido, la canalización agrega los descodificadores necesarios para convertir el origen en un tipo sin comprimir. Un codificador tiene una secuencia de entrada y una de salida. El codificador recibe datos de entrada y genera datos codificados según la configuración y el formato establecidos por la aplicación antes de la sesión de codificación. El formato del flujo de salida se describe mediante un tipo de medio.

Esta sección contiene los temas siguientes.



| Tema                                                                              | Descripción                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)                  | Explica cómo crear el codificador.                                                         |
| [Propiedades de codificación](configuring-the-encoder.md)                                 | Explica cómo configurar el codificador estableciendo las propiedades adecuadas en el MFT del codificador. |
| [Negociación de tipos de medios en el codificador](media-type-negotiation-on-the-encoder.md) | Explica cómo establecer tipos de medios de entrada y salida en el codificador.                            |
| [Configuración de un codificador WMV](configuring-a-wmv-encoder.md)                         | Explica cómo configurar un codificador Windows Media Video (WMV).                              |
| [Establecimiento de un tipo de salida para un codificador WMA](configuring-a-wma-encoder.md)          | Explica cómo establecer un tipo de salida en un Windows Media Audio (WMA).                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



