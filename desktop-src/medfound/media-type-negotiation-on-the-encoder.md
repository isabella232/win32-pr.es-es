---
description: Negociación de tipos de medios en el codificador
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Negociación de tipos de medios en el codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ac5dd5a107633feba4ce2a74da7e9aea7e9f71d51be1b5cad5b85ab4adda35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941515"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Negociación de tipos de medios en el codificador

En Microsoft Media Foundation, los codificadores se implementan [como transformaciones](media-foundation-transforms.md) de Media Foundation (MFT) con una entrada y una salida. Antes de una sesión de codificación, un codificador debe conocer las características de la secuencia que recibirá como entrada y el formato de la secuencia que producirá como salida. Debe establecer los tipos de medios de entrada y salida y las características relacionadas antes de pasar datos a través del codificador. Debe proporcionar los formatos de entrada y salida especificando los GUID de tipo multimedia [](media-type-attributes.md) adecuados y establecer las características del flujo de salida estableciendo los atributos de tipo multimedia [pertinentes](media-type-guids.md) en el tipo de medio de salida. Un codificador recién creado con instancias no tiene ningún tipo de medio establecido.

El tipo de medio de entrada es un formato sin comprimir, como audio PCM o vídeo RGB. Los tipos de formato que usa el codificador se limitan a los descritos por las estructuras **VIDEOINFOHEADER** **y WAVEFORMATEX.** Para obtener más información sobre estas estructuras, consulte la documentación Windows SDK. Media Foundation proporciona funciones auxiliares para crear tipos de medios a partir de estructuras de formato. Por ejemplo, la función [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) inicializa un tipo de vídeo a partir de una estructura **VIDEOINFOHEADER** y la función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) inicializa un tipo de vídeo a partir de una **estructuraWAVEATEX** **oWAVEATEXTENSIBLE.** Para obtener más información, vea [Conversiones de tipos de medios.](media-type-conversions.md) Debe establecer el tipo de medio de entrada en el codificador mediante una llamada [**a IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

El tipo de medio de salida es el formato de compresión utilizado en el archivo o flujo de origen final. Solo puede establecer el tipo de medio de salida disponible después de establecer el tipo de medio de entrada. Puede recuperar los tipos de salida admitidos llamando a [**MFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en un bucle hasta que el codificador devuelva **MF E NO MORE \_ \_ \_ \_ TYPES**. Incremente el índice de tipo con cada iteración. Cuando encuentre un tipo de medio adecuado, establezca el tipo de medio de salida mediante una llamada [**a IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

El factor determinante para elegir el tipo de medio de salida depende del tipo de codificación y de los requisitos de codificación. Por ejemplo, para las secuencias de audio codificadas en CBR, desea buscar un tipo de medio que coincida con la entrada y tenga una velocidad de bits lo más cercana posible a un valor de destino.

Si desea usar un modo de codificación distinto de CBR, debe establecer el modo y, a continuación, enumerar los tipos de salida para ese modo, ya que el codificador cambia los tipos de salida admitidos en función del modo establecido. Las propiedades que controlan el modo de codificación son [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) y [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Por ejemplo, si va a enumerar tipos de salida para la codificación de calidad VBR, el tipo de medio depende del valor de calidad que decida usar. Para obtener información sobre cómo establecer estas propiedades, vea [Propiedades de codificación](configuring-the-encoder.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 



