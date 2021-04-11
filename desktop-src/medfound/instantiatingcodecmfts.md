---
description: Crear instancias del códec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Crear instancias del códec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275501"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="346ec-103">Crear instancias del códec MFTs</span><span class="sxs-lookup"><span data-stu-id="346ec-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="346ec-104">[Media Foundation transformaciones](media-foundation-transforms.md) (MFTs) son objetos com que implementan la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="346ec-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="346ec-105">Una MFT es un objeto para transformar los datos multimedia como parte de una canalización.</span><span class="sxs-lookup"><span data-stu-id="346ec-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="346ec-106">Una canalización es un gráfico acíclicos dirigido, compuesto por orígenes multimedia, transformaciones multimedia y receptores multimedia.</span><span class="sxs-lookup"><span data-stu-id="346ec-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="346ec-107">Una canalización procesa los datos multimedia de streaming de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="346ec-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="346ec-108">Aunque se puede crear una instancia de MFTs y usar independientemente de la infraestructura de canalización Media Foundation, es preferible usar el marco de MediaFoundation siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="346ec-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="346ec-109">Puede crear un MFT de códec mediante una llamada a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="346ec-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="346ec-110">Debe pasar el identificador de clase de MFT, el identificador de interfaz de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)y un puntero a un puntero **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="346ec-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="346ec-111">Los identificadores de clase del códec MFTs se definen como constantes en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="346ec-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="346ec-112">La constante para el identificador de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) es IID \_ IMFTransform.</span><span class="sxs-lookup"><span data-stu-id="346ec-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="346ec-113">En el ejemplo de código siguiente se muestra cómo crear una instancia de un MFT de códec:</span><span class="sxs-lookup"><span data-stu-id="346ec-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="346ec-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="346ec-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346ec-115">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="346ec-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
