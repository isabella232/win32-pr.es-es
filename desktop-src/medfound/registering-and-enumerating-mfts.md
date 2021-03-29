---
description: En esta sección se describe cómo enumerar las transformaciones de Media Foundation y cómo registrar una MFT personalizada para que las aplicaciones puedan detectarla.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registro y enumeración de MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001443"
---
# <a name="registering-and-enumerating-mfts"></a>Registro y enumeración de MFTs

En esta sección se describe cómo enumerar las transformaciones de Media Foundation y cómo registrar una MFT personalizada para que las aplicaciones puedan detectarla.

-   [Enumerar MFTs](#registering-and-enumerating-mfts)
-   [Registrando MFTs](#registering-mfts)
-   [Temas relacionados](#related-topics)

## <a name="enumerating-mfts"></a>Enumerar MFTs

Para detectar MFTs que están registradas en el sistema, una aplicación puede llamar a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

> [!Note]  
> Esta función requiere a Windows 7. Antes de Windows 7, las aplicaciones deben usar la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en su lugar.

 

Esta función toma la siguiente información como entrada:

-   Categoría de MFT que se va a enumerar, como descodificador de vídeo o descodificador de audio.
-   Formato de entrada o de salida que se va a comparar.
-   Marcas que especifican condiciones de búsqueda adicionales.

La función devuelve una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uno de los cuales representa una MFT que coincide con los criterios de la enumeración.

Por ejemplo, el código siguiente enumera los descodificadores de Windows Media Video:


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



De forma predeterminada, algunos tipos de MFT se excluyen de la enumeración, incluidos los MFTs asincrónicos, MFTs de hardware y MFTs con restructing de campo de uso. Se excluyen porque requieren un tratamiento especial de algún tipo. Use el parámetro *Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para cambiar el valor predeterminado. Por ejemplo, para incluir hardware MFTs en los resultados de la enumeración, establezca la marca de **\_ \_ \_ hardware marcador de enumeración de MFT** :


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>Registrando MFTs

Cuando se registra una transformación de Media Foundation (MFT), se escriben dos tipos de información en el registro:

-   El CLSID de MFT, de modo que los clientes puedan llamar a **CoCreateInstance** o **CoGetClassObject** para crear una instancia de MFT. Esta entrada del registro sigue el formato estándar para los generadores de clases COM. Para obtener más información, vea la documentación de Windows SDK del modelo de objetos componentes (COM).
-   Información que permite a una aplicación enumerar MFTs por categoría funcional.

Para crear las entradas de enumeración de MFT en el registro, llame a la función [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . Puede incluir la siguiente información sobre la MFT:

-   La categoría de la MFT, como descodificador de vídeo o codificador de vídeo. Para obtener una lista de categorías, consulte la [**\_ categoría MFT**](mft-category.md).
-   Una lista de los formatos de entrada y salida que admite MFT. Cada formato se define mediante un tipo principal y un subtipo. (Para obtener información más detallada sobre el formato, el cliente debe crear la MFT y llamar a los métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ). El cargador de topología utiliza esta información cuando resuelve una topología parcial.

Para quitar las entradas del registro, llame a [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

En el código siguiente se muestra cómo registrar una MFT. En este ejemplo se da por supuesto que la MFT es un efecto de vídeo que admite los mismos formatos para la entrada y la salida.


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Campo de restricciones de uso](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



