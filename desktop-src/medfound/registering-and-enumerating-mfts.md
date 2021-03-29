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
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="a8abc-103">Registro y enumeración de MFTs</span><span class="sxs-lookup"><span data-stu-id="a8abc-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="a8abc-104">En esta sección se describe cómo enumerar las transformaciones de Media Foundation y cómo registrar una MFT personalizada para que las aplicaciones puedan detectarla.</span><span class="sxs-lookup"><span data-stu-id="a8abc-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="a8abc-105">Enumerar MFTs</span><span class="sxs-lookup"><span data-stu-id="a8abc-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="a8abc-106">Registrando MFTs</span><span class="sxs-lookup"><span data-stu-id="a8abc-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="a8abc-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8abc-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="a8abc-108">Enumerar MFTs</span><span class="sxs-lookup"><span data-stu-id="a8abc-108">Enumerating MFTs</span></span>

<span data-ttu-id="a8abc-109">Para detectar MFTs que están registradas en el sistema, una aplicación puede llamar a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="a8abc-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="a8abc-110">Esta función requiere a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8abc-110">This function requires to Windows 7.</span></span> <span data-ttu-id="a8abc-111">Antes de Windows 7, las aplicaciones deben usar la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a8abc-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="a8abc-112">Esta función toma la siguiente información como entrada:</span><span class="sxs-lookup"><span data-stu-id="a8abc-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="a8abc-113">Categoría de MFT que se va a enumerar, como descodificador de vídeo o descodificador de audio.</span><span class="sxs-lookup"><span data-stu-id="a8abc-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="a8abc-114">Formato de entrada o de salida que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="a8abc-114">An input or output format to match.</span></span>
-   <span data-ttu-id="a8abc-115">Marcas que especifican condiciones de búsqueda adicionales.</span><span class="sxs-lookup"><span data-stu-id="a8abc-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="a8abc-116">La función devuelve una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uno de los cuales representa una MFT que coincide con los criterios de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a8abc-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="a8abc-117">Por ejemplo, el código siguiente enumera los descodificadores de Windows Media Video:</span><span class="sxs-lookup"><span data-stu-id="a8abc-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


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



<span data-ttu-id="a8abc-118">De forma predeterminada, algunos tipos de MFT se excluyen de la enumeración, incluidos los MFTs asincrónicos, MFTs de hardware y MFTs con restructing de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="a8abc-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="a8abc-119">Se excluyen porque requieren un tratamiento especial de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="a8abc-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="a8abc-120">Use el parámetro *Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para cambiar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8abc-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="a8abc-121">Por ejemplo, para incluir hardware MFTs en los resultados de la enumeración, establezca la marca de **\_ \_ \_ hardware marcador de enumeración de MFT** :</span><span class="sxs-lookup"><span data-stu-id="a8abc-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


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



## <a name="registering-mfts"></a><span data-ttu-id="a8abc-122">Registrando MFTs</span><span class="sxs-lookup"><span data-stu-id="a8abc-122">Registering MFTs</span></span>

<span data-ttu-id="a8abc-123">Cuando se registra una transformación de Media Foundation (MFT), se escriben dos tipos de información en el registro:</span><span class="sxs-lookup"><span data-stu-id="a8abc-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="a8abc-124">El CLSID de MFT, de modo que los clientes puedan llamar a **CoCreateInstance** o **CoGetClassObject** para crear una instancia de MFT.</span><span class="sxs-lookup"><span data-stu-id="a8abc-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="a8abc-125">Esta entrada del registro sigue el formato estándar para los generadores de clases COM.</span><span class="sxs-lookup"><span data-stu-id="a8abc-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="a8abc-126">Para obtener más información, vea la documentación de Windows SDK del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="a8abc-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="a8abc-127">Información que permite a una aplicación enumerar MFTs por categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="a8abc-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="a8abc-128">Para crear las entradas de enumeración de MFT en el registro, llame a la función [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="a8abc-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="a8abc-129">Puede incluir la siguiente información sobre la MFT:</span><span class="sxs-lookup"><span data-stu-id="a8abc-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="a8abc-130">La categoría de la MFT, como descodificador de vídeo o codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a8abc-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="a8abc-131">Para obtener una lista de categorías, consulte la [**\_ categoría MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="a8abc-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="a8abc-132">Una lista de los formatos de entrada y salida que admite MFT.</span><span class="sxs-lookup"><span data-stu-id="a8abc-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="a8abc-133">Cada formato se define mediante un tipo principal y un subtipo.</span><span class="sxs-lookup"><span data-stu-id="a8abc-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="a8abc-134">(Para obtener información más detallada sobre el formato, el cliente debe crear la MFT y llamar a los métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ). El cargador de topología utiliza esta información cuando resuelve una topología parcial.</span><span class="sxs-lookup"><span data-stu-id="a8abc-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="a8abc-135">Para quitar las entradas del registro, llame a [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="a8abc-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="a8abc-136">En el código siguiente se muestra cómo registrar una MFT.</span><span class="sxs-lookup"><span data-stu-id="a8abc-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="a8abc-137">En este ejemplo se da por supuesto que la MFT es un efecto de vídeo que admite los mismos formatos para la entrada y la salida.</span><span class="sxs-lookup"><span data-stu-id="a8abc-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a8abc-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8abc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8abc-139">Campo de restricciones de uso</span><span class="sxs-lookup"><span data-stu-id="a8abc-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="a8abc-140">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="a8abc-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



