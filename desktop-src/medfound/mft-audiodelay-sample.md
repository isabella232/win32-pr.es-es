---
description: Ejemplo de AudioDelay de MFT \_
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Ejemplo de MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659837"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="0349b-103">Ejemplo de AudioDelay de MFT \_</span><span class="sxs-lookup"><span data-stu-id="0349b-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="0349b-104">Muestra cómo implementar un efecto de audio como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="0349b-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="0349b-105">El MFT de retraso de audio acepta el audio PCM como entrada, aplica un efecto de retraso (eco) y genera los datos de audio modificados.</span><span class="sxs-lookup"><span data-stu-id="0349b-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="0349b-106">API mostradas</span><span class="sxs-lookup"><span data-stu-id="0349b-106">APIs Demonstrated</span></span>

<span data-ttu-id="0349b-107">Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="0349b-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="0349b-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="0349b-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="0349b-109">Uso</span><span class="sxs-lookup"><span data-stu-id="0349b-109">Usage</span></span>

<span data-ttu-id="0349b-110">El \_ ejemplo AudioDelay de MFT crea un archivo DLL que es un servidor com para la MFT.</span><span class="sxs-lookup"><span data-stu-id="0349b-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="0349b-111">Antes de usar la MFT, debe registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="0349b-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="0349b-112">Puede usar la herramienta TopoEdit para crear una topología que incluya el MFT de retardo de audio.</span><span class="sxs-lookup"><span data-stu-id="0349b-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="0349b-113">Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="0349b-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="0349b-114">También puede modificar el [ejemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar la MFT.</span><span class="sxs-lookup"><span data-stu-id="0349b-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="0349b-115">Tendrá que modificar la función AddBranchToPartialTopology en Player. cpp.</span><span class="sxs-lookup"><span data-stu-id="0349b-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="0349b-116">Cambie la siguiente línea de:</span><span class="sxs-lookup"><span data-stu-id="0349b-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="0349b-117">Por:</span><span class="sxs-lookup"><span data-stu-id="0349b-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="0349b-118">El valor CLSID \_ DelayMFT se declara en el archivo de encabezado AudioDelayUuids. h de la \_ carpeta de ejemplo MFT AudioDelay.</span><span class="sxs-lookup"><span data-stu-id="0349b-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="0349b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0349b-119">Requirements</span></span>



| <span data-ttu-id="0349b-120">Producto</span><span class="sxs-lookup"><span data-stu-id="0349b-120">Product</span></span>                                                        | <span data-ttu-id="0349b-121">Versión</span><span class="sxs-lookup"><span data-stu-id="0349b-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0349b-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0349b-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0349b-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0349b-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0349b-124">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0349b-124">Downloading the Sample</span></span>

<span data-ttu-id="0349b-125">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span><span class="sxs-lookup"><span data-stu-id="0349b-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0349b-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0349b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0349b-127">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0349b-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0349b-128">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="0349b-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="0349b-129">\_Ejemplo de escala de grises de MFT</span><span class="sxs-lookup"><span data-stu-id="0349b-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="0349b-130">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="0349b-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
