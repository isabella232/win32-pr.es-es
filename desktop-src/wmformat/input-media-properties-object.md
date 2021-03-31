---
title: Objeto de propiedades de medios de entrada
description: Objeto de propiedades de medios de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- SDK de Windows Media Format, objetos de propiedades de medios de entrada
- Advanced Systems Format (ASF), objetos de propiedades de medios de entrada
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de entrada
- objetos, objetos de propiedades de medios de entrada
- objetos de propiedades de medios de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904398"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="a1996-108">Objeto de propiedades de medios de entrada</span><span class="sxs-lookup"><span data-stu-id="a1996-108">Input Media Properties Object</span></span>

<span data-ttu-id="a1996-109">Un objeto de propiedades de medios de entrada creado por el objeto de escritor admite las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1996-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="a1996-110">Se tiene acceso a estas interfaces mediante una llamada a **QueryInterface** en una de las interfaces del objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="a1996-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="a1996-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="a1996-111">Interface</span></span>                                        | <span data-ttu-id="a1996-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1996-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1996-113">**IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a1996-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="a1996-114">Recupera las propiedades de un flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1996-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="a1996-115">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a1996-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="a1996-116">Se usa como la interfaz base para las otras interfaces de propiedad de medios (entrada, salida y vídeo).</span><span class="sxs-lookup"><span data-stu-id="a1996-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="a1996-117">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a1996-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="a1996-118">Administra las propiedades de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1996-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="a1996-119">Se trata de una interfaz opcional, disponible solo para secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1996-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1996-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1996-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1996-121">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="a1996-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="a1996-122">**Objeto de Writer**</span><span class="sxs-lookup"><span data-stu-id="a1996-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




