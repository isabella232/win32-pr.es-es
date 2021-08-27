---
description: Creación de instancias de un MFT de codificador
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Creación de instancias de un MFT de codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40337bbef63cf243777978d1672a60de5ebfba8874b3cce0271ca06ccf4ab38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974274"
---
# <a name="instantiating-an-encoder-mft"></a>Creación de instancias de un MFT de codificador

En Microsoft Media Foundation, los codificadores se implementan [como transformaciones Media Foundation](media-foundation-transforms.md) (MFT). Antes de crear un codificador, primero debe encontrar el codificador más adecuado para sus necesidades.

-   Windows Códecs de audio multimedia

    Categoría: **CODIFICADOR DE AUDIO CATEGORÍA \_ \_ \_ MFT**

    Tipo principal: AUDIO \_ MFMediaType

    SubTipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Códecs de vídeo multimedia

    Categoría: **CODIFICADOR DE VÍDEO DE CATEGORÍA \_ \_ \_ MFT**

    Tipo principal: VÍDEO \_ MFMediaType

    Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Media Foundation proporciona varias funciones a las que la aplicación puede llamar para enumerar los distintos codificadores disponibles en el sistema. Los codificadores se registran como objetos COM y la entrada del Registro sigue el formato estándar para los generadores de clases COM. El Registro mantiene los CLSID para los codificadores, que se clasifican por el formato multimedia (audio o vídeo). Los identificadores de clase de Windows codificadores multimedia se definen como constantes en el archivo de encabezado wmcodecdsp.h. En Media Foundation, los codificadores se pueden registrar mediante llamadas a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) especificando la categoría, los tipos de entrada admitidos y los tipos de salida admitidos. Tras el registro correcto a través de estas funciones, las funciones de enumeración de Media Foundation las MTA.

Para crear una instancia de un MFT de codificador, una aplicación tiene las siguientes opciones.

-   Cree el MFT del codificador directamente y reciba un puntero a la [**interfaz DETRANSFORMTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Para obtener más información, vea [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Cree una instancia del objeto de activación para el MFT del codificador y reciba un puntero a la interfaz [**DEACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Para obtener más información, [vea Usar objetos de activación de un codificador.](using-an-encoder-s-activation-objects.md)

Si la aplicación usa componentes [asf](pipeline-layer-asf-components.md) de capa de canalización para codificar un archivo en formato ASF, debe insertar el MFT del codificador en la canalización como un nodo de transformación. Al crear el nodo de transformación en la topología de codificación, puede establecer el tipo de objeto como un puntero a la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o al [**objeto IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Media Foundation proporciona objetos de activación para Windows codificadores multimedia para que se puedan establecer cómodamente como nodo de transformación en la topología de codificación. Cuando se resuelve la topología, la sesión multimedia usa el objeto de activación para crear una instancia del MFT del codificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 



