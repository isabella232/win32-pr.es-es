---
title: Interfaces necesarias (Reproductor de Windows Media SDK)
description: Obtenga información sobre las interfaces necesarias que Reproductor de Windows Media implementa en DirectShow o Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Reproductor de Windows Media complementos, interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406098"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="d3ae0-108">Interfaces necesarias (Reproductor de Windows Media SDK)</span><span class="sxs-lookup"><span data-stu-id="d3ae0-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="d3ae0-109">Reproductor de Windows Media representa audio y vídeo mediante una de las siguientes canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="d3ae0-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="d3ae0-110">DirectShow</span></span>
-   <span data-ttu-id="d3ae0-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3ae0-111">Media Foundation</span></span>

<span data-ttu-id="d3ae0-112">En Microsoft Windows XP y versiones anteriores, el reproductor usa DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="d3ae0-113">En Windows Vista, el Reproductor a veces usa DirectShow y, a veces, usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="d3ae0-114">Un complemento DSP implementa algunas o todas las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3ae0-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="d3ae0-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-115">**IMediaObject**</span></span>
-   <span data-ttu-id="d3ae0-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="d3ae0-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-117">**IMFTransform**</span></span>
-   <span data-ttu-id="d3ae0-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-118">**IMFGetService**</span></span>
-   <span data-ttu-id="d3ae0-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="d3ae0-120">Un complemento que implementa **IMediaObject** e **IWMPPluginEnable** se puede ejecutar en la canalización de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="d3ae0-121">También se puede ejecutar en la canalización Media Foundation dentro de un contenedor proporcionado por Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="d3ae0-122">Un complemento de este tipo se denomina objeto multimedia (DMO) de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="d3ae0-123">Es habitual pensar que un DMO es análogo a un objeto de filtro en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="d3ae0-124">La documentación de DMO se encuentra en la sección DirectShow de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="d3ae0-125">Un complemento que implementa **IMFTransform** y **IMFGetService** se puede ejecutar de forma nativa (no se requiere ningún contenedor) en la Media Foundation ejecución.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="d3ae0-126">Un complemento de este tipo se denomina Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="d3ae0-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d3ae0-127">La documentación de MFT se encuentra en Media Foundation sección de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="d3ae0-128">Un complemento que implementa **IMediaObject**, **IWMPPluginEnable,** **IMFTransform** y **IMFGetService** se puede ejecutar en la canalización DirectShow y también se puede ejecutar de forma nativa en la canalización Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="d3ae0-129">Este tipo de complemento, que se denomina complemento DSP de modo *dual,* puede desempeñar el rol de DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="d3ae0-130">Cuando Reproductor de Windows Media un complemento DSP de modo dual en la canalización de Media Foundation, primero consulta la interfaz **DETRANSFORM.**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="d3ae0-131">Si se produce un error en esa consulta, Reproductor de Windows Media consultas para la **interfaz IMediaObject.**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="d3ae0-132">Si la **consulta IMediaObject** se realiza correctamente, el complemento se encapsula y se agrega a la Media Foundation ejecución.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="d3ae0-133">Independientemente de la canalización, cualquier complemento de DSP que permita al usuario establecer propiedades debe implementar **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3ae0-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3ae0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3ae0-135">**Introducción al desarrollador del complemento DSP**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="d3ae0-136">**Interfaces de complemento DE DSP**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d3ae0-137">**Empaquetado del complemento DE DSP**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




