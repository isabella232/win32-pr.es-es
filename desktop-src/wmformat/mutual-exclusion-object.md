---
title: Objeto de exclusión mutua
description: Objeto de exclusión mutua
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- SDK de Windows Media Format, objetos de exclusión mutua
- Advanced Systems Format (ASF), objetos de exclusión mutua
- ASF (formato de sistemas avanzados), objetos de exclusión mutua
- objetos, objetos de exclusión mutua
- exclusión mutua, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149119"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="942a4-108">Objeto de exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="942a4-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="942a4-109">Un objeto de exclusión mutua se utiliza para especificar un número de secuencias, de las cuales solo se puede entregar una a la vez.</span><span class="sxs-lookup"><span data-stu-id="942a4-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="942a4-110">Se puede usar de varias maneras, como proporcionar una secuencia de audio en varios idiomas como la banda sonora para un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="942a4-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="942a4-111">La exclusión mutua es una parte opcional de un perfil.</span><span class="sxs-lookup"><span data-stu-id="942a4-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="942a4-112">Se pueden crear objetos de exclusión mutua para la información de exclusión mutua existente en un perfil o se pueden crear vacíos, listos para recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="942a4-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="942a4-113">Los objetos de exclusión mutua no pueden existir independientemente de un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="942a4-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="942a4-114">Para guardar el contenido de un objeto de exclusión mutua, debe llamar a [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="942a4-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="942a4-115">Para crear un objeto de exclusión mutua, use uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="942a4-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="942a4-116">Método</span><span class="sxs-lookup"><span data-stu-id="942a4-116">Method</span></span>                                                                              | <span data-ttu-id="942a4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="942a4-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="942a4-118">**IWMProfile::CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="942a4-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="942a4-119">Crea un objeto de exclusión mutua sin datos.</span><span class="sxs-lookup"><span data-stu-id="942a4-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="942a4-120">**IWMProfile::GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="942a4-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="942a4-121">Crea un objeto de exclusión mutua rellenado con datos de un perfil.</span><span class="sxs-lookup"><span data-stu-id="942a4-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="942a4-122">Usa el índice de exclusión mutua para identificar la información de exclusión mutua deseada.</span><span class="sxs-lookup"><span data-stu-id="942a4-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="942a4-123">Ambos métodos de la tabla anterior establecen un puntero a una interfaz **IWMMutualExclusion** .</span><span class="sxs-lookup"><span data-stu-id="942a4-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="942a4-124">La interfaz **IWMStreamList** es heredada por **IWMMutualExclusion** y nunca es necesario tener acceso a ella directamente.</span><span class="sxs-lookup"><span data-stu-id="942a4-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="942a4-125">La otra interfaz del objeto de exclusión mutua se puede obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="942a4-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="942a4-126">Cada objeto de exclusión mutua admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="942a4-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="942a4-127">Interfaz</span><span class="sxs-lookup"><span data-stu-id="942a4-127">Interface</span></span>                                          | <span data-ttu-id="942a4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="942a4-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="942a4-129">**IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="942a4-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="942a4-130">Establece y recupera el tipo de exclusión mutua que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="942a4-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="942a4-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="942a4-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="942a4-132">Organiza los flujos en registros, que se pueden usar para crear escenarios complejos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="942a4-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="942a4-133">Hereda todos los métodos de **IWMMutualExclusion**.</span><span class="sxs-lookup"><span data-stu-id="942a4-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="942a4-134">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="942a4-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="942a4-135">Administra la lista de flujos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="942a4-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="942a4-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="942a4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942a4-137">**Exclusión mutua**</span><span class="sxs-lookup"><span data-stu-id="942a4-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="942a4-138">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="942a4-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="942a4-139">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="942a4-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




