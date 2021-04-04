---
title: Priorización de flujos
description: Priorización de flujos
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, priorización de flujos
- Advanced Systems Format (ASF), priorización de flujos
- ASF (formato de sistemas avanzados), priorización de flujo
- SDK de Windows Media Format, orden de prioridad para secuencias
- Advanced Systems Format (ASF), orden de prioridad de las secuencias
- ASF (formato de sistemas avanzados), orden de prioridad para flujos
- flujos, priorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077332"
---
# <a name="stream-prioritization"></a><span data-ttu-id="c99df-110">Priorización de flujos</span><span class="sxs-lookup"><span data-stu-id="c99df-110">Stream Prioritization</span></span>

<span data-ttu-id="c99df-111">Al crear un archivo ASF, puede especificar un orden de prioridad para sus flujos constituyentes.</span><span class="sxs-lookup"><span data-stu-id="c99df-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="c99df-112">Si transmite por secuencias un archivo con prioridad y el ancho de banda disponible no es suficiente para ofrecer todas las secuencias, el lector quitará los flujos en orden de prioridad inverso.</span><span class="sxs-lookup"><span data-stu-id="c99df-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="c99df-113">De este modo, puede garantizar que las secuencias más importantes del archivo no se quitarán debido a problemas de red.</span><span class="sxs-lookup"><span data-stu-id="c99df-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="c99df-114">La priorización de flujo se configura con un objeto de priorización de flujo y se agrega al perfil.</span><span class="sxs-lookup"><span data-stu-id="c99df-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="c99df-115">Un perfil puede contener solo un objeto de priorización de flujo.</span><span class="sxs-lookup"><span data-stu-id="c99df-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c99df-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c99df-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c99df-117">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="c99df-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="c99df-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c99df-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c99df-119">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c99df-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c99df-120">**IWMProfile3::RemoveStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c99df-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="c99df-121">**IWMProfile3::SetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c99df-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c99df-122">**Interfaz IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c99df-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c99df-123">**Usar la priorización de flujos**</span><span class="sxs-lookup"><span data-stu-id="c99df-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




