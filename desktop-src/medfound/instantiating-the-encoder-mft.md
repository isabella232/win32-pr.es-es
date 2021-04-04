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
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="a2302-103">Crear instancias de una MFT del codificador</span><span class="sxs-lookup"><span data-stu-id="a2302-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="a2302-104">En Microsoft Media Foundation, los codificadores se implementan como [transformaciones Media Foundation](media-foundation-transforms.md) (MFTs).</span><span class="sxs-lookup"><span data-stu-id="a2302-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="a2302-105">Antes de crear un codificador, primero debe encontrar el codificador que mejor se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="a2302-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="a2302-106">Códecs de audio de Windows Media</span><span class="sxs-lookup"><span data-stu-id="a2302-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="a2302-107">Categoría: **\_ categoría MFT \_ , \_ codificador de audio**</span><span class="sxs-lookup"><span data-stu-id="a2302-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="a2302-108">Tipo principal: MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="a2302-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="a2302-109">SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="a2302-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="a2302-110">Códecs de vídeo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="a2302-110">Windows Media video codecs</span></span>

    <span data-ttu-id="a2302-111">Categoría: **categoría de MFT \_ \_ \_ codificador de vídeo**</span><span class="sxs-lookup"><span data-stu-id="a2302-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="a2302-112">Tipo principal: vídeo de MFMediaType \_</span><span class="sxs-lookup"><span data-stu-id="a2302-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="a2302-113">SubType: MFVideoFormat \_ Wvc1, MFVideoFormat \_ Wmv3, MFVideoFormat wmv2 \_ , MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="a2302-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="a2302-114">Media Foundation proporciona varias funciones a las que la aplicación puede llamar para enumerar los distintos codificadores disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a2302-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="a2302-115">Los codificadores se registran como objetos COM y la entrada del registro sigue el formato estándar para los generadores de clases COM.</span><span class="sxs-lookup"><span data-stu-id="a2302-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="a2302-116">El registro mantiene los CLSID de los codificadores, que se clasifican por el formato multimedia (audio o vídeo).</span><span class="sxs-lookup"><span data-stu-id="a2302-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="a2302-117">Los identificadores de clase de los codificadores de Windows Media se definen como constantes en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a2302-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="a2302-118">En Media Foundation, los codificadores se pueden registrar a través de llamadas a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) especificando categoría, los tipos de entrada admitidos y los tipos de salida admitidos.</span><span class="sxs-lookup"><span data-stu-id="a2302-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="a2302-119">Cuando el registro se realiza correctamente a través de estas funciones, las funciones de enumeración Media Foundation consideran las MFTs.</span><span class="sxs-lookup"><span data-stu-id="a2302-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="a2302-120">Para crear una instancia de una MFT del codificador, una aplicación tiene las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="a2302-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="a2302-121">Cree la MFT del codificador directamente y reciba un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="a2302-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="a2302-122">Para obtener más información, vea [crear un codificador mediante CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="a2302-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="a2302-123">Cree una instancia del objeto de activación para la MFT del codificador y reciba un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a2302-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="a2302-124">Para obtener más información, vea [usar los objetos de activación de un codificador](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a2302-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="a2302-125">Si la aplicación usa [componentes ASF de capa de canalización](pipeline-layer-asf-components.md) para codificar un archivo en formato ASF, debe insertar la MFT del codificador en la canalización como nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="a2302-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="a2302-126">Al crear el nodo de transformación en la topología de codificación, puede establecer el tipo de objeto como un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a2302-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="a2302-127">Media Foundation proporciona objetos de activación para los codificadores de Windows Media de modo que se puedan establecer adecuadamente como nodo de transformación en la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="a2302-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="a2302-128">Cuando se resuelve la topología, la sesión multimedia utiliza el objeto de activación para crear una instancia de la MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="a2302-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2302-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2302-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2302-130">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="a2302-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



