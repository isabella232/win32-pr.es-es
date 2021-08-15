---
description: Establecimiento de un tipo de salida para un codificador WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Establecimiento de un tipo de salida para un codificador WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f2731a081138bda30ab3e81f01d353e0348f4d3586fd4c02878b62a7f04393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880576"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Establecimiento de un tipo de salida para un codificador WMA

Para crear un tipo de salida válido para un Windows Audio multimedia (WMA), debe tener la siguiente información:

-   Subtipo de audio que representa el formato WMA codificado. Consulte [GUID de subtipo de audio.](audio-subtype-guids.md)
-   Propiedades de configuración que se establecerán en el codificador.

    Las propiedades de configuración se documentan en la documentación Windows Media Audio y Video Codec y LAS API de DSP. Para obtener más información, vea "Propiedades de secuencia de audio" en [Propiedades de codificación](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista o versiones posteriores

Para obtener un tipo de salida válido para el codificador, realice los pasos siguientes.

1.  Use las [**funciones MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) [**o MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para crear una instancia del codificador.
2.  Consulte el codificador para la **interfaz IPropertyStore.**
3.  Use la **interfaz IPropertyStore** para configurar el codificador.
4.  Recupere los tipos de salida admitidos mediante una llamada a [**MFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en un bucle hasta que el codificador devuelva **MF E NO MORE \_ \_ \_ \_ TYPES** y elija el tipo de medio de destino. I
5.  Llame [**a IMFTransform::SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) establecer el tipo de medio de compresión en el codificador.

### <a name="windows-7"></a>Windows 7

Para obtener un tipo de salida válido para el codificador en Windows 7, Media Foundation proporciona la [**función MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) Una aplicación debe pasar el subtipo de audio necesario que repeste la WMA codificada y las propiedades de codificación. Las propiedades son necesarias porque el codificador cambia los tipos de salida admitidos en función del modo establecido.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)solo se admite para [la codificación de velocidad de bits constante.](constant-bit-rate-encoding.md)

 

Si la llamada se realiza correctamente, la aplicación recibe una lista de punteros IUnknown de los tipos de medios de salida admitidos en un [**objeto RECORDSETCollection.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) Para establecer el tipo de medio de salida, busque el que coincida con el tipo de destino y llame a [**IMFTransform::SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) establecer el tipo de medio de compresión en el codificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 



