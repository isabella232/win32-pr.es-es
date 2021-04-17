---
description: Para convertir archivos multimedia en formato ASF, puede usar codificadores de Windows Media. Para usar estos codificadores, se deben registrar con el sistema.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Crear un codificador mediante CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696865"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Crear un codificador mediante CoCreateInstance

Para convertir archivos multimedia en formato ASF, puede usar codificadores de Windows Media. Para usar estos codificadores, se deben registrar con el sistema. Los codificadores se implementan como [transformaciones de Media Foundation](media-foundation-transforms.md) (MFTs) y deben exponer la interfaz IMFTransform. En este tema se describe cómo una aplicación puede obtener un puntero a la interfaz IMFTransform del codificador MFT necesaria y crear una instancia de él para su uso.

Para obtener información sobre el registro del codificador, consulte [crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md).

-   [Uso de la interfaz IMFTransform de un codificador](#creating-an-encoder-by-using-cocreateinstance)
    -   [Ejemplo de creación del codificador](#encoder-creation-example)
-   [Temas relacionados](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Uso de la interfaz IMFTransform de un codificador

Tras registrar correctamente los codificadores de Windows Media con el sistema, una aplicación puede enumerar los codificadores mediante una llamada a [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Para buscar el codificador correcto, debe especificar lo siguiente:

-   GUID que representa la categoría, que es el codificador de **\_ \_ audio \_ de categoría de MFT** o el **\_ \_ \_ codificador de vídeo de categoría MFT**.

-   Formato que se va a comparar. Esto se establece en la estructura de información de tipo de registro de MFT que especifica el tipo principal y el subtipo del tipo de medio en el que el codificador generará los ejemplos. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) Esta estructura se pasa en el parámetro *pOutputType* . Para obtener información sobre los tipos admitidos, consulte [GUID de tipo de medio](media-type-guids.md).

    > [!Note]  
    > La información del tipo de entrada en el parámetro *pInputType* no es necesaria. Esto se debe a que la aplicación conoce el tipo de entrada y el codificador espera que el flujo de entrada esté en un formato sin comprimir.

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) devuelve una matriz de punteros [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para el codificador MFTs que coinciden con los criterios de búsqueda. Puede crear una instancia de un codificador llamando a la función de COM **CoCreateInstance** y pasando el CLSID del codificador que desea usar. Esta función devuelve un puntero a la interfaz **IMFTransform** que representa el codificador. Para obtener más información sobre esta llamada de función, vea la documentación de Windows SDK del modelo de objetos componentes (COM).

### <a name="encoder-creation-example"></a>Ejemplo de creación del codificador

En el ejemplo de código siguiente se muestra cómo crear un codificador de audio o vídeo.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



