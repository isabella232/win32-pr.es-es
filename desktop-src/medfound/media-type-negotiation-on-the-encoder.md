---
description: Negociación de tipo de medio en el codificador
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Negociación de tipo de medio en el codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7845e9d50c5d418198dc0e08313e2e9329ffab8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003424"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Negociación de tipo de medio en el codificador

En Microsoft Media Foundation, los codificadores se implementan como [transformaciones Media Foundation](media-foundation-transforms.md) (MFTs) con una entrada y una salida. Antes de una sesión de codificación, un codificador debe conocer las características de la secuencia que recibirá como entrada y el formato de la secuencia que generará como salida. Debe establecer los tipos de medios de entrada y salida, así como las características relacionadas, antes de pasar los datos a través del codificador. Debe proporcionar los formatos de entrada y salida especificando los GUID de [tipo de medio](media-type-guids.md) adecuados y estableciendo las características del flujo de salida mediante el establecimiento de los [atributos de tipo de medio](media-type-attributes.md) correspondientes en el tipo de medio de salida. Un codificador con una instancia recién creada no tiene ningún tipo de medio establecido.

El tipo de medio de entrada es un formato sin comprimir, como audio PCM o vídeo RGB. Los tipos de formato que utiliza el codificador se limitan a los descritos por las estructuras **VIDEOINFOHEADER** y **WAVEFORMATEX** . Para obtener más información acerca de estas estructuras, vea la documentación de Windows SDK. Media Foundation proporciona funciones auxiliares para crear tipos de medios a partir de estructuras de formato. Por ejemplo, la función [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Inicializa un tipo de vídeo a partir de una estructura **VIDEOINFOHEADER** , y la función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) Inicializa un tipo de vídeo a partir de una estructura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** . Para obtener más información, vea [conversiones de tipo de medio](media-type-conversions.md). Debe establecer el tipo de medio de entrada en el codificador llamando a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

El tipo de medio de salida es el formato de compresión utilizado en la secuencia o el archivo de origen final. Solo puede establecer el tipo de medio de salida disponible después de establecer el tipo de medio de entrada. Puede recuperar los tipos de salida admitidos llamando a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en un bucle hasta que el codificador devuelva **MF \_ E \_ ningún \_ \_ tipo más**. Incremente el índice de tipo con cada iteración. Cuando encuentre un tipo de medio adecuado, establezca el tipo de medio de salida llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

El factor de decisión a la hora de elegir el tipo de medio de salida depende del tipo de codificación y de los requisitos de codificación. Por ejemplo, en el caso de las secuencias de audio con codificación CBR, desea encontrar un tipo de medio que coincida con la entrada y que tenga una velocidad de bits lo más cercana posible a un valor de destino.

Si desea utilizar un modo de codificación distinto de CBR, debe establecer el modo y, a continuación, enumerar los tipos de salida para ese modo, porque el codificador cambia los tipos de salida admitidos en función del conjunto de modos. Las propiedades que controlan el modo de codificación son [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) y [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Por ejemplo, si se enumeran los tipos de salida para la codificación de calidad VBR, el tipo de medio depende del valor de calidad que decida usar. Para obtener información sobre cómo establecer estas propiedades, consulte [propiedades de codificación](configuring-the-encoder.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



