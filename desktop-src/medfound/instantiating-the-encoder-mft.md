---
description: Crear instancias de una MFT del codificador
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Crear instancias de una MFT del codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277838"
---
# <a name="instantiating-an-encoder-mft"></a>Crear instancias de una MFT del codificador

En Microsoft Media Foundation, los codificadores se implementan como [transformaciones Media Foundation](media-foundation-transforms.md) (MFTs). Antes de crear un codificador, primero debe encontrar el codificador que mejor se adapte a sus necesidades.

-   Códecs de audio de Windows Media

    Categoría: **\_ categoría MFT \_ , \_ codificador de audio**

    Tipo principal: MFMediaType \_ audio

    SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Códecs de vídeo de Windows Media

    Categoría: **categoría de MFT \_ \_ \_ codificador de vídeo**

    Tipo principal: vídeo de MFMediaType \_

    SubType: MFVideoFormat \_ Wvc1, MFVideoFormat \_ Wmv3, MFVideoFormat wmv2 \_ , MFVideoFormat \_ WMV1

Media Foundation proporciona varias funciones a las que la aplicación puede llamar para enumerar los distintos codificadores disponibles en el sistema. Los codificadores se registran como objetos COM y la entrada del registro sigue el formato estándar para los generadores de clases COM. El registro mantiene los CLSID de los codificadores, que se clasifican por el formato multimedia (audio o vídeo). Los identificadores de clase de los codificadores de Windows Media se definen como constantes en el archivo de encabezado wmcodecdsp. h. En Media Foundation, los codificadores se pueden registrar a través de llamadas a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) especificando categoría, los tipos de entrada admitidos y los tipos de salida admitidos. Cuando el registro se realiza correctamente a través de estas funciones, las funciones de enumeración Media Foundation consideran las MFTs.

Para crear una instancia de una MFT del codificador, una aplicación tiene las siguientes opciones.

-   Cree la MFT del codificador directamente y reciba un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Para obtener más información, vea [crear un codificador mediante CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Cree una instancia del objeto de activación para la MFT del codificador y reciba un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Para obtener más información, vea [usar los objetos de activación de un codificador](using-an-encoder-s-activation-objects.md).

Si la aplicación usa [componentes ASF de capa de canalización](pipeline-layer-asf-components.md) para codificar un archivo en formato ASF, debe insertar la MFT del codificador en la canalización como nodo de transformación. Al crear el nodo de transformación en la topología de codificación, puede establecer el tipo de objeto como un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Media Foundation proporciona objetos de activación para los codificadores de Windows Media de modo que se puedan establecer adecuadamente como nodo de transformación en la topología de codificación. Cuando se resuelve la topología, la sesión multimedia utiliza el objeto de activación para crear una instancia de la MFT del codificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



