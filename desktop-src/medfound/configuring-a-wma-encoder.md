---
description: Establecer un tipo de salida para un codificador WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Establecer un tipo de salida para un codificador WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153668"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Establecer un tipo de salida para un codificador WMA

Para crear un tipo de salida válido para un codificador Windows Media Audio (WMA), debe tener la siguiente información:

-   El subtipo de audio que repesents el formato WMA codificado. Vea [GUID de subtipo de audio](audio-subtype-guids.md).
-   Propiedades de configuración que se van a establecer en el codificador.

    Las propiedades de configuración se documentan en la documentación del códec de Windows Media Audio y vídeo y de las API de DSP. Para obtener más información, vea "propiedades de secuencia de audio" en [propiedades de codificación](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista o posterior

Para obtener un tipo de salida válido para el codificador, realice los pasos siguientes.

1.  Utilice la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para crear una instancia del codificador.
2.  Consulte el codificador para la interfaz **IPropertyStore** .
3.  Use la interfaz **IPropertyStore** para configurar el codificador.
4.  Recupere los tipos de salida admitidos mediante una llamada a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en un bucle hasta que el codificador devuelva **MF \_ e \_ no haya \_ más \_ tipos** y elija el tipo de medio de destino. I
5.  Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.

### <a name="windows-7"></a>Windows 7

Para obtener un tipo de salida válido para el codificador en Windows 7, Media Foundation proporciona la función [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Una aplicación debe pasar el subtipo de audio que repesents los WMA codificados y las propiedades de codificación. Las propiedades son necesarias porque el codificador cambia los tipos de salida admitidos en función del conjunto de modos.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)solo se admite para la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md).

 

Si la llamada se realiza correctamente, la aplicación recibe una lista de punteros IUnknown de los tipos de medios de salida admitidos en un objeto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) . Para establecer el tipo de medio de salida, busque el que coincida con su tipo de destino y llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



