---
title: Objeto de perfil
description: Objeto de perfil
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- SDK de Windows Media Format, objetos de perfil
- Advanced Systems Format (ASF), objetos de perfil
- ASF (formato de sistemas avanzados), objetos de perfil
- objetos, objetos de perfil
- perfiles, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103904441"
---
# <a name="profile-object"></a><span data-ttu-id="31881-108">Objeto de perfil</span><span class="sxs-lookup"><span data-stu-id="31881-108">Profile Object</span></span>

<span data-ttu-id="31881-109">Un objeto de perfil administra la configuración de un perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="31881-110">Los objetos de perfil se pueden crear para los datos de perfil existentes o se pueden crear vacíos, listos para recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="31881-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="31881-111">El objeto de lector también crea un objeto de perfil (y el objeto de lector sincrónico) cuando se carga un archivo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="31881-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="31881-112">En este caso, el objeto se rellena con la información de perfil almacenada en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="31881-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="31881-113">Para guardar el contenido de un objeto de perfil, debe llamar a [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span><span class="sxs-lookup"><span data-stu-id="31881-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="31881-114">Un perfil contiene varios objetos que controlan diversos aspectos del perfil (por ejemplo, secuencias).</span><span class="sxs-lookup"><span data-stu-id="31881-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="31881-115">Todos estos objetos se subordinan al objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="31881-116">No cree estos objetos con funciones de creación como lo haría con los objetos principales de este SDK.</span><span class="sxs-lookup"><span data-stu-id="31881-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="31881-117">En su lugar, las interfaces del objeto de perfil contienen métodos que crean los objetos subordinados.</span><span class="sxs-lookup"><span data-stu-id="31881-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="31881-118">Para crear un objeto de perfil, llame a uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="31881-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="31881-119">Método</span><span class="sxs-lookup"><span data-stu-id="31881-119">Method</span></span>                                                                                | <span data-ttu-id="31881-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="31881-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31881-121">**IWMProfileManager::CreateEmptyProfile**</span><span class="sxs-lookup"><span data-stu-id="31881-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="31881-122">Crea un objeto de perfil sin datos de perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="31881-123">**IWMProfileManager::LoadProfileByData**</span><span class="sxs-lookup"><span data-stu-id="31881-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="31881-124">Crea un objeto de perfil rellenado con datos de un perfil guardado como una cadena.</span><span class="sxs-lookup"><span data-stu-id="31881-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="31881-125">Esta es la única manera de crear un objeto de perfil con datos de un perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="31881-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="31881-126">**IWMProfileManager::LoadProfileByID**</span><span class="sxs-lookup"><span data-stu-id="31881-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="31881-127">Crea un objeto de perfil rellenado con datos de un perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="31881-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="31881-128">Utiliza el GUID para identificar el perfil del sistema deseado.</span><span class="sxs-lookup"><span data-stu-id="31881-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="31881-129">**IWMProfileManager::LoadSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="31881-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="31881-130">Crea un objeto de perfil rellenado con datos de un perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="31881-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="31881-131">Usa el índice de perfil para identificar el perfil de sistema deseado.</span><span class="sxs-lookup"><span data-stu-id="31881-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="31881-132">Todos los métodos de la tabla anterior establecen un puntero a una interfaz **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="31881-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="31881-133">Las demás interfaces del objeto de perfil se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="31881-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="31881-134">Cada objeto de perfil admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="31881-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="31881-135">Interfaz</span><span class="sxs-lookup"><span data-stu-id="31881-135">Interface</span></span>                                  | <span data-ttu-id="31881-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="31881-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31881-137">**IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="31881-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="31881-138">Administra una lista de idiomas admitidos por un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="31881-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="31881-139">**IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="31881-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="31881-140">Controla el tamaño máximo de los paquetes de un archivo.</span><span class="sxs-lookup"><span data-stu-id="31881-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="31881-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="31881-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="31881-142">Controla el tamaño mínimo de los paquetes de un archivo.</span><span class="sxs-lookup"><span data-stu-id="31881-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="31881-143">Hereda todos los métodos de **IWMPacketSize**.</span><span class="sxs-lookup"><span data-stu-id="31881-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="31881-144">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="31881-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="31881-145">Controla la configuración básica y los objetos incluidos en un perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="31881-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="31881-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="31881-147">Recupera el identificador único global (GUID) asociado al perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="31881-148">Hereda todos los métodos de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="31881-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="31881-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="31881-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="31881-150">Controla la información de priorización de flujo y uso compartido de ancho de banda en un perfil.</span><span class="sxs-lookup"><span data-stu-id="31881-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="31881-151">Hereda todos los métodos de **IWMProfile** y **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="31881-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="31881-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31881-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31881-153">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="31881-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="31881-154">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="31881-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="31881-155">**Perfiles**</span><span class="sxs-lookup"><span data-stu-id="31881-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




