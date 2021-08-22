---
description: En esta sección se describe cómo enumerar Media Foundation transformaciones y cómo registrar un MFT personalizado para que las aplicaciones puedan detectarlo.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registro y enumeración de MTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101834"
---
# <a name="registering-and-enumerating-mfts"></a>Registro y enumeración de MTA

En esta sección se describe cómo enumerar Media Foundation transformaciones y cómo registrar un MFT personalizado para que las aplicaciones puedan detectarlo.

-   [Enumeración de MTA](#registering-and-enumerating-mfts)
-   [Registro de MTA](#registering-mfts)
-   [Temas relacionados](#related-topics)

## <a name="enumerating-mfts"></a>Enumeración de MTA

Para detectar los MFT registrados en el sistema, una aplicación puede llamar a la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

> [!Note]  
> Esta función requiere Windows 7. Antes de Windows 7, las aplicaciones deben usar la [**función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en su lugar.

 

Esta función toma la siguiente información como entrada:

-   Categoría de MFT que se enumera, como descodificador de vídeo o descodificador de audio.
-   Formato de entrada o salida que se debe coincidir.
-   Marcas que especifican condiciones de búsqueda adicionales.

La función devuelve una matriz de punteros [**DE TIPO DEACTIVATE,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) cada uno de los cuales representa un MFT que coincide con los criterios de enumeración.

Por ejemplo, el código siguiente enumera Windows descodificadores de Vídeo multimedia:


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



De forma predeterminada, algunos tipos de MFT se excluyen de la enumeración, incluidos los MFT asincrónicos, los MFT de hardware y los MFT con reestructuraciones de campo de uso. Se excluyen porque todos requieren un control especial de algún tipo. Use el *parámetro Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para cambiar el valor predeterminado. Por ejemplo, para incluir las MFT de hardware en los resultados de enumeración, establezca la marca DE **HARDWARE MFT \_ ENUM \_ FLAG: \_**


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



## <a name="registering-mfts"></a>Registro de MTA

Al registrar una transformación Media Foundation transformación (MFT), se escriben dos tipos de información en el registro:

-   CLSID de MFT, para que los clientes puedan llamar a **CoCreateInstance** o **CoGetClassObject** para crear una instancia de MFT. Esta entrada del Registro sigue el formato estándar para los generadores de clases COM. Para obtener más información, consulte la documentación Windows SDK para component Object Model (COM).
-   Información que permite a una aplicación enumerar las MTA por categoría funcional.

Para crear las entradas de enumeración de MFT en el Registro, llame a la [**función MFTRegister.**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) Puede incluir la siguiente información sobre MFT:

-   Categoría del MFT, como el descodificador de vídeo o el codificador de vídeo. Para obtener una lista de categorías, vea [**CATEGORÍA DE MFT \_**](mft-category.md).
-   Lista de formatos de entrada y salida que admite MFT. Cada formato se define mediante un tipo principal y un subtipo. (Para obtener información de formato más detallada, el cliente debe crear el MFT y llamar a [**los métodos DETRANSFORMTRANSFORM).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) El cargador de topologías usa esta información cuando resuelve una topología parcial.

Para quitar las entradas del Registro, llame a [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

El código siguiente muestra cómo registrar un MFT. En este ejemplo se supone que MFT es un efecto de vídeo que admite los mismos formatos para la entrada y la salida.


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

[Restricciones de campo de uso](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



