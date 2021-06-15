---
description: Para convertir archivos multimedia al formato ASF, puede usar codificadores de Windows Media. Obtenga información sobre cómo crear un codificador mediante CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creación de un codificador mediante CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068471"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="3c145-104">Creación de un codificador mediante CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="3c145-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="3c145-105">Para convertir archivos multimedia al formato ASF, puede usar codificadores de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3c145-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="3c145-106">Para usar estos codificadores, deben estar registrados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3c145-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="3c145-107">Los codificadores se implementan [como Media Foundation](media-foundation-transforms.md) transformaciones (MTA) y deben exponer la interfaz DETRANSFORMTransform.</span><span class="sxs-lookup"><span data-stu-id="3c145-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="3c145-108">En este tema se describe cómo una aplicación puede obtener un puntero a la interfaz DETRANSFORMTransform del codificador MFT necesaria y crear instancias de ella para su uso.</span><span class="sxs-lookup"><span data-stu-id="3c145-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="3c145-109">Para obtener información sobre el registro del codificador, vea [Creación de instancias de Un codificador MFT.](instantiating-the-encoder-mft.md)</span><span class="sxs-lookup"><span data-stu-id="3c145-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="3c145-110">Usar la interfaz DETRANSFORM de un codificador</span><span class="sxs-lookup"><span data-stu-id="3c145-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="3c145-111">Ejemplo de creación del codificador</span><span class="sxs-lookup"><span data-stu-id="3c145-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="3c145-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c145-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="3c145-113">Usar la interfaz DETRANSFORM de un codificador</span><span class="sxs-lookup"><span data-stu-id="3c145-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="3c145-114">Tras el registro correcto de codificadores de Windows Media con el sistema, una aplicación puede enumerar los codificadores mediante una llamada a [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span><span class="sxs-lookup"><span data-stu-id="3c145-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="3c145-115">Para buscar el codificador adecuado, debe especificar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3c145-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="3c145-116">GUID que representa la categoría , que es **MFT \_ CATEGORY AUDIO \_ \_ ENCODER** o **MFT CATEGORY VIDEO \_ \_ \_ ENCODER**.</span><span class="sxs-lookup"><span data-stu-id="3c145-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="3c145-117">Formato que se debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="3c145-117">The format to match.</span></span> <span data-ttu-id="3c145-118">Esto se establece en la estructura [**\_ MFT REGISTER \_ TYPE \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que especifica el tipo principal y el subtipo del tipo de medio en el que el codificador generará ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3c145-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="3c145-119">Esta estructura se pasa en el *parámetro pOutputType.*</span><span class="sxs-lookup"><span data-stu-id="3c145-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="3c145-120">Para obtener información sobre los tipos admitidos, vea [GUID de tipo multimedia.](media-type-guids.md)</span><span class="sxs-lookup"><span data-stu-id="3c145-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="3c145-121">No se requiere la información del tipo de entrada en el parámetro *pInputType.*</span><span class="sxs-lookup"><span data-stu-id="3c145-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="3c145-122">Esto se debe a que la aplicación conoce el tipo de entrada y el codificador espera que el flujo de entrada esté en un formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="3c145-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="3c145-123">[**MFTEnum devuelve**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) una matriz de punteros [**MFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para los MFT del codificador que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3c145-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="3c145-124">Puede crear instancias de un codificador llamando a la función COM **CoCreateInstance** y pasando el CLSID del codificador que desea usar.</span><span class="sxs-lookup"><span data-stu-id="3c145-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="3c145-125">Esta función devuelve un puntero a la **interfaz DETRANSFORMTransform** que representa el codificador.</span><span class="sxs-lookup"><span data-stu-id="3c145-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="3c145-126">Para obtener más información sobre esta llamada de función, vea la documentación Windows SDK del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="3c145-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="3c145-127">Ejemplo de creación del codificador</span><span class="sxs-lookup"><span data-stu-id="3c145-127">Encoder Creation Example</span></span>

<span data-ttu-id="3c145-128">En el ejemplo de código siguiente se muestra cómo crear un codificador de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="3c145-128">The following code example shows how to create an audio or video encoder.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3c145-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c145-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c145-130">Creación de instancias de un MFT de codificador</span><span class="sxs-lookup"><span data-stu-id="3c145-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="3c145-131">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="3c145-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



