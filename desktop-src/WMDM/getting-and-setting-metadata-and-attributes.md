---
title: Obtener y establecer metadatos y atributos
description: Obtener y establecer metadatos y atributos
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media Administrador de dispositivos, atributos
- Administrador de dispositivos, atributos
- aplicaciones de escritorio, atributos
- proveedores de servicios, atributos
- Guía de programación, atributos
- attributes
- Administrador de dispositivos de Windows Media, metadatos
- Administrador de dispositivos, metadatos
- aplicaciones de escritorio, metadatos
- proveedores de servicios, metadatos
- Guía de programación, metadatos
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903577"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="0903c-115">Obtener y establecer metadatos y atributos</span><span class="sxs-lookup"><span data-stu-id="0903c-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="0903c-116">Una aplicación puede obtener dos tipos de información sobre un dispositivo o almacenamiento: atributos y metadatos.</span><span class="sxs-lookup"><span data-stu-id="0903c-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="0903c-117">Los atributos son valores booleanos más sencillos que, por lo general, describen la información del sistema de archivos, por ejemplo, si un almacenamiento tiene objetos secundarios, si se puede cambiar de nombre, leer o eliminar, etc.</span><span class="sxs-lookup"><span data-stu-id="0903c-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="0903c-118">Los atributos se recuperan como valores de marcas mediante una llamada a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span><span class="sxs-lookup"><span data-stu-id="0903c-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="0903c-119">Los atributos se establecen mediante una llamada a [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="0903c-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="0903c-120">Una aplicación también puede solicitar datos más complejos (numéricos, de cadena u otros tipos de datos) como *metadatos*.</span><span class="sxs-lookup"><span data-stu-id="0903c-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="0903c-121">Los valores de los metadatos se identifican mediante nombres de cadena únicos.</span><span class="sxs-lookup"><span data-stu-id="0903c-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="0903c-122">Windows Media Administrador de dispositivos define una lista de constantes de cadena que se pueden usar para solicitar valores. Estos valores definidos se muestran en [constantes de metadatos](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0903c-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="0903c-123">Un proveedor de servicios puede definir sus propias constantes, pero una aplicación que realiza la llamada debe tener en cuenta estas definiciones para solicitar o establecer estos valores de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="0903c-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="0903c-124">La aplicación solicita los metadatos mediante una llamada a [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="0903c-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="0903c-125">Un aspecto importante de la obtención y configuración de metadatos y atributos es comprender de dónde proceden los valores recuperados.</span><span class="sxs-lookup"><span data-stu-id="0903c-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="0903c-126">El proveedor de servicios o el dispositivo pueden obtener estos valores desde muchos lugares diferentes, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0903c-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="0903c-127">Del encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-127">From the file header.</span></span> <span data-ttu-id="0903c-128">Por ejemplo, en un archivo ASF, la velocidad de bits se almacena en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="0903c-129">De los valores establecidos explícitamente por la aplicación cuando se llama a un método.</span><span class="sxs-lookup"><span data-stu-id="0903c-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="0903c-130">Estos valores se pueden guardar en un almacén de metadatos externo en el proveedor de servicios o en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="0903c-131">Este almacén puede persistir o no cuando el dispositivo se desconecta o se apaga.</span><span class="sxs-lookup"><span data-stu-id="0903c-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="0903c-132">Por ejemplo, las clasificaciones de recuento de juegos y de estrellas de usuario suelen almacenarse en almacenes externos en el equipo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="0903c-133">Examinando la información proporcionada por el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="0903c-133">By examining information provided by the file system.</span></span> <span data-ttu-id="0903c-134">Por ejemplo, si un archivo es de solo lectura o si una carpeta tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0903c-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="0903c-135">Abriendo y analizando los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="0903c-136">Es importante tener en cuentan que una propiedad puede almacenarse en más de una ubicación (dentro del encabezado de archivo y también en un almacén local) y que puede ser o no modificable.</span><span class="sxs-lookup"><span data-stu-id="0903c-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="0903c-137">Por ejemplo, el cambio de una descripción de archivo puede ser o no persistente; Si el proveedor de servicios almacena la descripción localmente, no se conservará en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0903c-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="0903c-138">Del mismo modo, si la descripción del archivo se toma del encabezado del archivo, la modificación solo será persistente si el proveedor de servicios o el dispositivo se abren y modifican los datos del encabezado.</span><span class="sxs-lookup"><span data-stu-id="0903c-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="0903c-139">La mayoría de las aplicaciones realizan un mejor intento cambiando los valores deseados, pero no dependen de las propiedades que se cambien de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="0903c-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="0903c-140">Más información sobre cómo obtener y establecer valores en las secciones adecuadas para desarrolladores de aplicaciones y desarrolladores de proveedores de servicios más adelante en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="0903c-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0903c-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0903c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0903c-142">**Tareas comunes a las aplicaciones y proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="0903c-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




