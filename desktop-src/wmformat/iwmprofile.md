---
title: Interfaz de IWMProfile
description: La interfaz IWMProfile es la interfaz principal para un objeto de perfil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Interfaz IWMProfile formato de Windows Media
- Interfaz IWMProfile formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105665885"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="97019-105">Interfaz de IWMProfile</span><span class="sxs-lookup"><span data-stu-id="97019-105">IWMProfile interface</span></span>

<span data-ttu-id="97019-106">La interfaz **IWMProfile** es la interfaz principal para un objeto de [*perfil*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="97019-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="97019-107">Un objeto de perfil se utiliza para configurar perfiles personalizados.</span><span class="sxs-lookup"><span data-stu-id="97019-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="97019-108">Puede usar **IWMProfile** para crear, eliminar o modificar objetos de configuración de la secuencia y objetos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="97019-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="97019-109">También puede establecer y recuperar información general sobre el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="97019-110">Para tener acceso a todas las características del objeto de perfil, debe usar [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), que hereda de **IWMProfile** y [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span><span class="sxs-lookup"><span data-stu-id="97019-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="97019-111">También se puede tener acceso a **IWMProfile** a través del objeto lector, donde puede usarlo para obtener información sobre las secuencias de un archivo que se carga en el lector.</span><span class="sxs-lookup"><span data-stu-id="97019-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="97019-112">Al tener acceso a **IWMProfile** desde el lector, puede realizar cambios en el perfil, pero ninguno de los cambios se puede guardar en el archivo.</span><span class="sxs-lookup"><span data-stu-id="97019-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="97019-113">A menudo resulta útil usar el perfil de un archivo existente como base de un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="97019-114">El lector sincrónico admite **IWMProfile** de la misma manera que el lector.</span><span class="sxs-lookup"><span data-stu-id="97019-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="97019-115">La información del perfil obtenida a través del lector o del lector sincrónico no procede de un archivo. prx.</span><span class="sxs-lookup"><span data-stu-id="97019-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="97019-116">El lector usa la información del archivo ASF para ensamblar las configuraciones de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="97019-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="97019-117">Por lo tanto, determinada información de perfil, como el nombre y la descripción, no está disponible a través del lector.</span><span class="sxs-lookup"><span data-stu-id="97019-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="97019-118">Hay varias maneras de obtener un puntero a una interfaz **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="97019-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="97019-119">El administrador de perfiles tiene métodos para crear un nuevo perfil y obtener acceso a los perfiles existentes.</span><span class="sxs-lookup"><span data-stu-id="97019-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="97019-120">Todos estos métodos establecen un puntero **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="97019-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="97019-121">Al leer un archivo, se puede obtener un puntero a **IWMProfile** llamando al método **QueryInterface** de cualquier interfaz de lector.</span><span class="sxs-lookup"><span data-stu-id="97019-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="97019-122">Del mismo modo, cualquier interfaz del objeto lector sincrónico puede obtener un puntero con una llamada a **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span><span class="sxs-lookup"><span data-stu-id="97019-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="97019-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="97019-123">Members</span></span>

<span data-ttu-id="97019-124">La interfaz **IWMProfile** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="97019-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97019-125">**IWMProfile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97019-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="97019-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="97019-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97019-127">Métodos</span><span class="sxs-lookup"><span data-stu-id="97019-127">Methods</span></span>

<span data-ttu-id="97019-128">La interfaz **IWMProfile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="97019-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="97019-129">Método</span><span class="sxs-lookup"><span data-stu-id="97019-129">Method</span></span>                                                                  | <span data-ttu-id="97019-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="97019-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97019-131">**AddMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="97019-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="97019-132">Agrega un objeto de exclusión mutua al perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="97019-133">**AddStream**</span><span class="sxs-lookup"><span data-stu-id="97019-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="97019-134">Agrega una secuencia al perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="97019-135">**CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="97019-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="97019-136">Crea un objeto de exclusión mutua para el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="97019-137">**CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="97019-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="97019-138">Crea un objeto de configuración de secuencia para el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="97019-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="97019-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="97019-140">Recupera la descripción del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="97019-141">**GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="97019-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="97019-142">Recupera un objeto de exclusión mutua del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="97019-143">**GetMutualExclusionCount**</span><span class="sxs-lookup"><span data-stu-id="97019-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="97019-144">Recupera el número de objetos de exclusión mutua en el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="97019-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="97019-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="97019-146">Recupera el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="97019-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="97019-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="97019-148">Recupera un flujo, utilizando un número de índice, del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="97019-149">**GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="97019-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="97019-150">Recupera una secuencia, usando el número de la secuencia, del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="97019-151">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="97019-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="97019-152">Recupera el número de flujos del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="97019-153">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="97019-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="97019-154">Recupera el número de versión de Microsoft Windows Media Services en el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="97019-155">**ReconfigStream**</span><span class="sxs-lookup"><span data-stu-id="97019-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="97019-156">Permite que los cambios realizados en una configuración de flujo se incluyan en el perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="97019-157">**RemoveMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="97019-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="97019-158">Quita un objeto de exclusión mutua del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="97019-159">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="97019-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="97019-160">Quita un flujo del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="97019-161">**RemoveStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="97019-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="97019-162">Quita un flujo del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="97019-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="97019-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="97019-164">Especifica la descripción del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="97019-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="97019-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="97019-166">Especifica el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="97019-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="97019-167">Para obtener información sobre las interfaces que se pueden obtener con el método QueryInterface de esta interfaz, vea el tema sobre el objeto en el que se implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="97019-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="97019-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="97019-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97019-169">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="97019-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="97019-170">**Interfaz IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="97019-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="97019-171">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="97019-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="97019-172">**Objeto del lector**</span><span class="sxs-lookup"><span data-stu-id="97019-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="97019-173">**Objeto del lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="97019-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="97019-174">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="97019-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

