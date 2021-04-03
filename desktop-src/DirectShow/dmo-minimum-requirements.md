---
description: Requisitos mínimos de DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisitos mínimos de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997919"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="cdf34-103">Requisitos mínimos de DMO</span><span class="sxs-lookup"><span data-stu-id="cdf34-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="cdf34-104">Cada DMO debe cumplir los siguientes requisitos mínimos:</span><span class="sxs-lookup"><span data-stu-id="cdf34-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="cdf34-105">Debe admitir la agregación.</span><span class="sxs-lookup"><span data-stu-id="cdf34-105">It must support aggregation.</span></span>
-   <span data-ttu-id="cdf34-106">Debe exponer la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="cdf34-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="cdf34-107">El modelo de subprocesos debe ser ' both '.</span><span class="sxs-lookup"><span data-stu-id="cdf34-107">The threading model must be 'both'.</span></span> <span data-ttu-id="cdf34-108">DMOs debe funcionar correctamente en un entorno de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="cdf34-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="cdf34-109">El efecto de audio DMOs debe ser compatible con la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) para su uso en DirectMusic y DirectSound.</span><span class="sxs-lookup"><span data-stu-id="cdf34-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="cdf34-110">Las siguientes interfaces se documentan en otro lugar, pero son útiles para muchos DMOs.</span><span class="sxs-lookup"><span data-stu-id="cdf34-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="cdf34-111">Sin embargo, no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="cdf34-111">They are not required, however.</span></span>

-   <span data-ttu-id="cdf34-112">**ISpecifyPropertyPages**, **IPropertyPage**: estas interfaces permiten a DMO proporcionar una página de propiedades para que el usuario establezca las propiedades.</span><span class="sxs-lookup"><span data-stu-id="cdf34-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="cdf34-113">**IPersistStream**: esta interfaz permite a DMO guardar su estado en un almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="cdf34-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="cdf34-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): estas interfaces permiten a un cliente configurar el formato de salida de un codificador y la configuración de compresión.</span><span class="sxs-lookup"><span data-stu-id="cdf34-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="cdf34-115">(Estas dos interfaces forman parte de la API de DirectShow, pero también se recomiendan para DMOs).</span><span class="sxs-lookup"><span data-stu-id="cdf34-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdf34-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdf34-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf34-117">Escritura de DMO</span><span class="sxs-lookup"><span data-stu-id="cdf34-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



