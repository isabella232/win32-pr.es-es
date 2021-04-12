---
title: Objeto de uso compartido de ancho de banda
description: Objeto de uso compartido de ancho de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- SDK de formato de Windows Media, objetos de uso compartido de ancho de banda
- Advanced Systems Format (ASF), ancho de banda Sharing Objects
- ASF (formato de sistemas avanzados), objetos de uso compartido de ancho de banda
- objetos, uso compartido de ancho de banda
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420289"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="850a0-108">Objeto de uso compartido de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="850a0-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="850a0-109">Un objeto de uso compartido de ancho de banda se usa para indicar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad de ancho de banda especificada entre ellas.</span><span class="sxs-lookup"><span data-stu-id="850a0-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="850a0-110">Se trata de un objeto meramente informativo; los objetos de este SDK no aplican mediante programación las velocidades de bits establecidas dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="850a0-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="850a0-111">La información de uso compartido de ancho de banda es una parte opcional de un perfil.</span><span class="sxs-lookup"><span data-stu-id="850a0-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="850a0-112">Se pueden crear objetos de uso compartido de ancho de banda para la información de uso compartido de ancho de banda existente en un perfil o se pueden crear vacíos, listos para recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="850a0-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="850a0-113">Los objetos de uso compartido de ancho de banda no pueden existir independientemente de un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="850a0-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="850a0-114">Para guardar el contenido de un objeto de uso compartido de ancho de banda, debe llamar a [**IWMProfile3:: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span><span class="sxs-lookup"><span data-stu-id="850a0-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="850a0-115">Para crear un objeto de uso compartido de ancho de banda, llame a uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="850a0-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="850a0-116">Método</span><span class="sxs-lookup"><span data-stu-id="850a0-116">Method</span></span>                                                                                  | <span data-ttu-id="850a0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="850a0-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="850a0-118">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="850a0-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="850a0-119">Crea un objeto de uso compartido de ancho de banda sin datos.</span><span class="sxs-lookup"><span data-stu-id="850a0-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="850a0-120">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="850a0-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="850a0-121">Crea un objeto de uso compartido de ancho de banda rellenado con datos de un perfil.</span><span class="sxs-lookup"><span data-stu-id="850a0-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="850a0-122">Usa el índice de uso compartido de ancho de banda para identificar la información de uso compartido de ancho de banda deseada.</span><span class="sxs-lookup"><span data-stu-id="850a0-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="850a0-123">Ambos métodos de la tabla anterior establecen un puntero a una interfaz **IWMBandwidthSharing** .</span><span class="sxs-lookup"><span data-stu-id="850a0-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="850a0-124">**IWMBandwidthSharing** hereda la interfaz **IWMStreamList** , por lo que no es necesario llamar a **QueryInterface** con este objeto.</span><span class="sxs-lookup"><span data-stu-id="850a0-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="850a0-125">Cada objeto de uso compartido de ancho de banda admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="850a0-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="850a0-126">Interfaz</span><span class="sxs-lookup"><span data-stu-id="850a0-126">Interface</span></span>                                          | <span data-ttu-id="850a0-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="850a0-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="850a0-128">**IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="850a0-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="850a0-129">Administra las propiedades de un grupo de secuencias que compartirán el ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="850a0-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="850a0-130">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="850a0-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="850a0-131">Administra la lista de secuencias que compartirán el ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="850a0-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="850a0-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="850a0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="850a0-133">**Uso compartido de ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="850a0-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="850a0-134">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="850a0-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="850a0-135">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="850a0-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




