---
title: Objeto del administrador de perfiles
description: Objeto del administrador de perfiles
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- SDK de Windows Media Format, objetos de administrador de perfiles
- Advanced Systems Format (ASF), objetos de administrador de perfiles
- ASF (formato de sistemas avanzados), objetos de administrador de perfiles
- objetos, objetos del administrador de perfiles
- perfiles, objetos
- perfiles, objetos de administrador de perfiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105714347"
---
# <a name="profile-manager-object"></a><span data-ttu-id="f58c4-109">Objeto del administrador de perfiles</span><span class="sxs-lookup"><span data-stu-id="f58c4-109">Profile Manager Object</span></span>

<span data-ttu-id="f58c4-110">Un perfil es un conjunto de parámetros de medios que se usan para crear un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f58c4-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="f58c4-111">El objeto de administrador de perfiles crea objetos de perfil para su edición.</span><span class="sxs-lookup"><span data-stu-id="f58c4-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="f58c4-112">Los objetos de perfil se pueden crear sin datos en ellos o compilados a partir de datos de perfil existentes.</span><span class="sxs-lookup"><span data-stu-id="f58c4-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="f58c4-113">El objeto de administrador de perfiles también proporciona métodos para enumerar códecs admitidos y consultar los códecs para obtener información.</span><span class="sxs-lookup"><span data-stu-id="f58c4-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="f58c4-114">El objeto de administrador de perfiles se crea mediante la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , que establece un puntero a una interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="f58c4-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="f58c4-115">Las demás interfaces del objeto de administrador de perfiles se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="f58c4-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="f58c4-116">El objeto de administrador de perfiles admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="f58c4-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="f58c4-117">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f58c4-117">Interface</span></span>                                                      | <span data-ttu-id="f58c4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f58c4-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f58c4-119">**IWMCodecInfo**</span><span class="sxs-lookup"><span data-stu-id="f58c4-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="f58c4-120">Recupera información acerca de los códecs admitidos y sus formatos.</span><span class="sxs-lookup"><span data-stu-id="f58c4-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="f58c4-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="f58c4-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="f58c4-122">Recupera los nombres de los códecs admitidos y las descripciones de sus formatos.</span><span class="sxs-lookup"><span data-stu-id="f58c4-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="f58c4-123">Hereda todos los métodos de **IWMCodecInfo**.</span><span class="sxs-lookup"><span data-stu-id="f58c4-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="f58c4-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="f58c4-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="f58c4-125">Recupera las propiedades de códec y los códecs de consultas para las características admitidas.</span><span class="sxs-lookup"><span data-stu-id="f58c4-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="f58c4-126">Hereda todos los métodos de **IWMCodecInfo** y **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="f58c4-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="f58c4-127">**IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="f58c4-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="f58c4-128">Crea nuevos perfiles, carga perfiles existentes y guarda perfiles personalizados.</span><span class="sxs-lookup"><span data-stu-id="f58c4-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="f58c4-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="f58c4-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="f58c4-130">Controla la versión de los perfiles del sistema enumerados por el administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="f58c4-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="f58c4-131">Hereda todos los métodos de **IWMProfileManager**.</span><span class="sxs-lookup"><span data-stu-id="f58c4-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="f58c4-132">**IWMProfileManagerLanguage**</span><span class="sxs-lookup"><span data-stu-id="f58c4-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="f58c4-133">Controla el idioma de los perfiles del sistema analizados por el administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="f58c4-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="f58c4-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f58c4-134">Remarks</span></span>

<span data-ttu-id="f58c4-135">Cuando se crea un objeto de administrador de perfiles, analiza todos los perfiles del sistema, lo que puede tardar varios segundos.</span><span class="sxs-lookup"><span data-stu-id="f58c4-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="f58c4-136">La creación y liberación de un administrador de perfiles cada vez que se necesita usar, afectará negativamente al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f58c4-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="f58c4-137">Debe crear un administrador de perfiles una vez en la aplicación y liberarlo solo cuando ya no tenga que usarlo.</span><span class="sxs-lookup"><span data-stu-id="f58c4-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f58c4-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f58c4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f58c4-139">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="f58c4-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="f58c4-140">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="f58c4-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="f58c4-141">**Perfiles**</span><span class="sxs-lookup"><span data-stu-id="f58c4-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




