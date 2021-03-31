---
title: Interfaces necesarias (SDK de Windows Media Player)
description: Interfaces necesarias
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904952"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="c122a-108">Interfaces necesarias (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="c122a-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="c122a-109">Windows Media Player representa audio y vídeo mediante una de las siguientes canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="c122a-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="c122a-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="c122a-110">DirectShow</span></span>
-   <span data-ttu-id="c122a-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c122a-111">Media Foundation</span></span>

<span data-ttu-id="c122a-112">En Microsoft Windows XP y versiones anteriores, el reproductor utiliza DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c122a-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="c122a-113">En Windows Vista, el reproductor a veces usa DirectShow y a veces usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c122a-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="c122a-114">Un complemento DSP implementa algunas o todas las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="c122a-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="c122a-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="c122a-115">**IMediaObject**</span></span>
-   <span data-ttu-id="c122a-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="c122a-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="c122a-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="c122a-117">**IMFTransform**</span></span>
-   <span data-ttu-id="c122a-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="c122a-118">**IMFGetService**</span></span>
-   <span data-ttu-id="c122a-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="c122a-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="c122a-120">Un complemento que implementa **IMediaObject** y **IWMPPluginEnable** puede ejecutarse en la canalización de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c122a-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="c122a-121">También puede ejecutarse en la canalización de Media Foundation dentro de un contenedor proporcionado por Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c122a-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="c122a-122">Un complemento de este tipo se denomina Microsoft DirectX media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="c122a-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="c122a-123">Es habitual considerar que un DMO es análogo a un objeto de filtro en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c122a-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="c122a-124">La documentación de DMO está en la sección de DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c122a-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="c122a-125">Un complemento que implementa **IMFTransform** y **IMFGetService** se puede ejecutar de forma nativa (no se requiere ningún contenedor) en la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c122a-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="c122a-126">Un complemento de este tipo se denomina Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="c122a-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="c122a-127">La documentación de MFT está en la sección Media Foundation del Windows SDK de.</span><span class="sxs-lookup"><span data-stu-id="c122a-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="c122a-128">Los complementos que implementan **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** y **IMFGetService** se pueden ejecutar en la canalización de DirectShow y también se pueden ejecutar de forma nativa en la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c122a-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="c122a-129">Este tipo de complemento, que se denomina un *complemento DSP de modo dual*, puede desempeñar el rol de un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="c122a-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="c122a-130">Cuando Windows Media Player usa un complemento DSP de modo dual en la canalización de Media Foundation, primero consulta la interfaz **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="c122a-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="c122a-131">Si se produce un error en la consulta, Windows Media Player consultas para la interfaz **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="c122a-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="c122a-132">Si la consulta **IMediaObject** se realiza correctamente, el complemento se ajusta y se agrega a la canalización Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c122a-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="c122a-133">Independientemente de la canalización, cualquier complemento de DSP que permita al usuario establecer propiedades debe implementar **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="c122a-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c122a-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c122a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c122a-135">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="c122a-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="c122a-136">**Interfaces de complemento de DSP**</span><span class="sxs-lookup"><span data-stu-id="c122a-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c122a-137">**Empaquetado de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="c122a-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




