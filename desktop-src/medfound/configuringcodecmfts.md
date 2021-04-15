---
description: Configuración de códecs MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configuración de códecs MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496828"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="01525-103">Configuración de códecs MFTs</span><span class="sxs-lookup"><span data-stu-id="01525-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="01525-104">En este tema se describe el proceso de configuración del códec MFTs.</span><span class="sxs-lookup"><span data-stu-id="01525-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="01525-105">Cada códec tiene procedimientos específicos, pero la información común a todos se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="01525-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="01525-106">Configuración de entradas y salidas de MFT</span><span class="sxs-lookup"><span data-stu-id="01525-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="01525-107">Cada MFT admite tipos de entrada y salida concretos.</span><span class="sxs-lookup"><span data-stu-id="01525-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="01525-108">Puede recuperar los tipos de entrada admitidos llamando a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)repetidamente, incrementando el índice de tipo con cada llamada.</span><span class="sxs-lookup"><span data-stu-id="01525-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="01525-109">Cuando encuentre un tipo adecuado, establezca el tipo de entrada mediante una llamada a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="01525-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="01525-110">Después, puede repetir el proceso para el tipo de salida mediante las llamadas a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) y [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="01525-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="01525-111">Debe consultar o establecer los tipos de salida disponibles solo después de establecer el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="01525-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="01525-112">Configuración del códec MFTs para la codificación</span><span class="sxs-lookup"><span data-stu-id="01525-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="01525-113">Todos los códecs de Windows Media Audio y vídeo admiten una variedad de características de codificación.</span><span class="sxs-lookup"><span data-stu-id="01525-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="01525-114">Estas características se configuran generalmente mediante el establecimiento de las propiedades en MFT mediante los métodos de la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="01525-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="01525-115">Algunas propiedades se configuran mediante interfaces de códec especializadas.</span><span class="sxs-lookup"><span data-stu-id="01525-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="01525-116">Estas interfaces se enumeran para cada códec en la sección [objetos de códec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="01525-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="01525-117">El orden general de las operaciones para configurar un MFT de codificación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="01525-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="01525-118">Configure las características del códec según sea necesario mediante los métodos de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="01525-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="01525-119">Use las interfaces MFT de códec para configurar características adicionales, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="01525-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="01525-120">Configure los tipos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="01525-120">Configure the input and output types.</span></span> <span data-ttu-id="01525-121">El orden en que deben configurarse los tipos varía en los códecs individuales.</span><span class="sxs-lookup"><span data-stu-id="01525-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="01525-122">Para obtener más información, consulte [trabajar con audio](workingwithaudio.md) y [trabajar con vídeo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="01525-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="01525-123">Configuración del códec MFTs para la descodificación</span><span class="sxs-lookup"><span data-stu-id="01525-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="01525-124">La descodificación es más sencilla que la codificación, ya que se admiten menos características de descodificador.</span><span class="sxs-lookup"><span data-stu-id="01525-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="01525-125">El orden general de las operaciones para configurar una MFT de descodificación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="01525-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="01525-126">Configure las características del descodificador según sea necesario mediante los métodos de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="01525-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="01525-127">Establezca el tipo de entrada en el tipo que se usa para la salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="01525-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="01525-128">Configure el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="01525-128">Configure the output type.</span></span> <span data-ttu-id="01525-129">Los tipos de salida admitidos son diferentes para las distintas entradas.</span><span class="sxs-lookup"><span data-stu-id="01525-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="01525-130">Es importante usar el mismo tipo de medio para la entrada del descodificador que se usó para la salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="01525-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="01525-131">Esto se debe a que los códecs de Windows Media Audio y vídeo usan formatos de medios con datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="01525-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="01525-132">Sin los datos de formato extendido, no se puede descodificar el contenido comprimido.</span><span class="sxs-lookup"><span data-stu-id="01525-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="01525-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01525-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01525-134">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="01525-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



