---
title: Objeto de configuración del flujo
description: Objeto de configuración del flujo
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- SDK de Windows Media Format, objetos de configuración de secuencia
- Advanced Systems Format (ASF), stream Configuration Objects
- ASF (formato de sistemas avanzados), objetos de configuración de secuencia
- objetos, objetos de configuración de secuencias
- objetos de configuración de secuencia
- flujos, objetos de configuración de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149127"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="0e359-109">Objeto de configuración del flujo</span><span class="sxs-lookup"><span data-stu-id="0e359-109">Stream Configuration Object</span></span>

<span data-ttu-id="0e359-110">Un objeto de configuración de secuencia se utiliza para especificar las propiedades de una secuencia de medios en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="0e359-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="0e359-111">Los objetos de configuración de secuencia se pueden crear para los flujos existentes en un perfil o se pueden crear vacíos, listos para recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="0e359-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="0e359-112">Los objetos de configuración de secuencia no pueden existir independientemente de un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="0e359-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="0e359-113">Para guardar el contenido de un objeto de configuración de secuencia, debe llamar a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar una nueva secuencia o [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para guardar los cambios realizados en una secuencia existente.</span><span class="sxs-lookup"><span data-stu-id="0e359-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="0e359-114">Para crear un objeto de configuración de secuencia, use uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0e359-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="0e359-115">Método</span><span class="sxs-lookup"><span data-stu-id="0e359-115">Method</span></span>                                                                | <span data-ttu-id="0e359-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e359-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e359-117">**IWMProfile::CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="0e359-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="0e359-118">Crea un objeto de configuración de secuencia sin datos.</span><span class="sxs-lookup"><span data-stu-id="0e359-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="0e359-119">**IWMProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="0e359-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="0e359-120">Crea un objeto de configuración de secuencia que se rellena con datos de un perfil.</span><span class="sxs-lookup"><span data-stu-id="0e359-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="0e359-121">Usa el índice de la secuencia para identificar el flujo deseado.</span><span class="sxs-lookup"><span data-stu-id="0e359-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="0e359-122">**IWMProfile::GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="0e359-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="0e359-123">Crea un objeto de configuración de secuencia que se rellena con datos de un perfil.</span><span class="sxs-lookup"><span data-stu-id="0e359-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="0e359-124">Utiliza el número de secuencia para identificar el flujo deseado.</span><span class="sxs-lookup"><span data-stu-id="0e359-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="0e359-125">Todos los métodos de la tabla anterior establecen un puntero a una interfaz **IWMStreamConfig** .</span><span class="sxs-lookup"><span data-stu-id="0e359-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="0e359-126">Las demás interfaces del objeto de configuración de la secuencia se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="0e359-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="0e359-127">El objeto de configuración de la secuencia admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="0e359-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="0e359-128">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0e359-128">Interface</span></span>                                        | <span data-ttu-id="0e359-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e359-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e359-130">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="0e359-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="0e359-131">Establece y recupera la estructura [**de \_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e359-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="0e359-132">**IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="0e359-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="0e359-133">Establece y recupera propiedades que no son necesarias para todas las secuencias, como la configuración de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="0e359-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="0e359-134">**IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="0e359-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="0e359-135">Establece y recupera toda la información básica sobre una secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e359-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="0e359-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="0e359-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="0e359-137">Configura los tipos de extensiones de unidad de datos asociados a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e359-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="0e359-138">Hereda todos los métodos de **IWMStreamConfig**.</span><span class="sxs-lookup"><span data-stu-id="0e359-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="0e359-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="0e359-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="0e359-140">Establece y recupera el idioma de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e359-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="0e359-141">Hereda todos los métodos de **IWMStreamConfig** y **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="0e359-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="0e359-142">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="0e359-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="0e359-143">Administra las propiedades de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e359-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="0e359-144">Se trata de una interfaz opcional y solo está disponible para las secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e359-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="0e359-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e359-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e359-146">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="0e359-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="0e359-147">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="0e359-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="0e359-148">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="0e359-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




