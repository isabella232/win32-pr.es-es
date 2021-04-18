---
title: Objeto de priorización de flujo
description: Objeto de priorización de flujo
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- SDK de Windows Media Format, objetos de priorización de secuencias
- Advanced Systems Format (ASF), objetos de priorización de secuencias
- ASF (formato de sistemas avanzados), objetos de priorización de secuencias
- objetos, objetos de priorización de secuencias
- objetos de priorización de flujo
- flujos, objetos de priorización de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105720128"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="af2ad-109">Objeto de priorización de flujo</span><span class="sxs-lookup"><span data-stu-id="af2ad-109">Stream Prioritization Object</span></span>

<span data-ttu-id="af2ad-110">Un objeto de priorización de flujo se utiliza para especificar un orden de importancia para las secuencias de un perfil.</span><span class="sxs-lookup"><span data-stu-id="af2ad-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="af2ad-111">Cuando no es posible la reproducción completa debido a las limitaciones de velocidad de bits, las secuencias de prioridad más baja serán las primeras que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="af2ad-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="af2ad-112">Los objetos de priorización de flujo se pueden crear para los datos de priorización de flujo existentes en un perfil o se pueden crear vacíos, listos para recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="af2ad-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="af2ad-113">Los objetos de priorización de flujo no pueden existir independientemente de un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="af2ad-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="af2ad-114">Para guardar el contenido de un objeto de priorización de flujo, debe llamar a [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span><span class="sxs-lookup"><span data-stu-id="af2ad-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="af2ad-115">Para crear un objeto de priorización de secuencia, use uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="af2ad-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="af2ad-116">Método</span><span class="sxs-lookup"><span data-stu-id="af2ad-116">Method</span></span>                                                                                          | <span data-ttu-id="af2ad-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2ad-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="af2ad-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="af2ad-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="af2ad-119">Crea un objeto de priorización de flujo sin datos.</span><span class="sxs-lookup"><span data-stu-id="af2ad-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="af2ad-120">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="af2ad-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="af2ad-121">Crea un objeto de priorización de flujo rellenado con datos del perfil.</span><span class="sxs-lookup"><span data-stu-id="af2ad-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="af2ad-122">Ambos métodos de la tabla anterior establecen un puntero a una interfaz **IWMStreamPrioritization** .</span><span class="sxs-lookup"><span data-stu-id="af2ad-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="af2ad-123">Esta es la única interfaz que admite el objeto de priorización de flujo.</span><span class="sxs-lookup"><span data-stu-id="af2ad-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="af2ad-124">Interfaz</span><span class="sxs-lookup"><span data-stu-id="af2ad-124">Interface</span></span>                                                  | <span data-ttu-id="af2ad-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2ad-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="af2ad-126">**IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="af2ad-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="af2ad-127">Administra la lista de secuencias en el objeto de priorización de flujo.</span><span class="sxs-lookup"><span data-stu-id="af2ad-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="af2ad-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af2ad-128">Remarks</span></span>

<span data-ttu-id="af2ad-129">Solo puede existir una priorización de flujo para un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="af2ad-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="af2ad-130">Si crea una nueva priorización de flujo para un perfil que ya contiene una priorización de flujo, se eliminará la antigua.</span><span class="sxs-lookup"><span data-stu-id="af2ad-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2ad-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af2ad-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2ad-132">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="af2ad-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="af2ad-133">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="af2ad-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="af2ad-134">**Usar la priorización de flujos**</span><span class="sxs-lookup"><span data-stu-id="af2ad-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




