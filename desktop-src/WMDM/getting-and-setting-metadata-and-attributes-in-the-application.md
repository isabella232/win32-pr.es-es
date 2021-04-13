---
title: Acceder a metadatos y atributos en la aplicación
description: Obtener y establecer metadatos y atributos en la aplicación
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Administrador de dispositivos de Windows Media, metadatos
- Administrador de dispositivos, metadatos
- Guía de programación, metadatos
- aplicaciones de escritorio, metadatos
- crear aplicaciones de Windows Media Administrador de dispositivos, metadatos
- metadata
- Windows Media Administrador de dispositivos, atributos
- Administrador de dispositivos, atributos
- Guía de programación, atributos
- aplicaciones de escritorio, atributos
- crear aplicaciones de Windows Media Administrador de dispositivos, atributos
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104358544"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="0ce47-115">Acceder a metadatos y atributos en la aplicación</span><span class="sxs-lookup"><span data-stu-id="0ce47-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="0ce47-116">En [obtener y establecer metadatos y atributos](getting-and-setting-metadata-and-attributes.md), se ofrece una explicación general de los metadatos y los atributos.</span><span class="sxs-lookup"><span data-stu-id="0ce47-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="0ce47-117">En esta sección se tratan las llamadas de método de aplicación específicas para recuperar o establecer valores.</span><span class="sxs-lookup"><span data-stu-id="0ce47-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="0ce47-118">Las aplicaciones pueden recuperar atributos o metadatos sobre un almacenamiento específico mediante una llamada a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="0ce47-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="0ce47-119">**GetMetadata** recupera una colección completa de todos los metadatos asociados a un almacenamiento y, a continuación, la aplicación puede enumerar todos los valores o solicitar valores específicos de la colección.</span><span class="sxs-lookup"><span data-stu-id="0ce47-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="0ce47-120">**GetSpecifiedMetadata** crea un objeto de metadatos en nombre del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="0ce47-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="0ce47-121">El autor de la llamada puede solicitar un subconjunto de los datos disponibles rellenando el parámetro *ppwszPropNames* con una matriz de las cadenas de propiedades de Windows Media administrador de dispositivos deseadas y el recuento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0ce47-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="0ce47-122">El objeto de metadatos devuelto se rellenará con las propiedades que se podrían recuperar.</span><span class="sxs-lookup"><span data-stu-id="0ce47-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="0ce47-123">Las propiedades que no se pudieron recuperar estarán ausentes.</span><span class="sxs-lookup"><span data-stu-id="0ce47-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="0ce47-124">Los metadatos se devuelven en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="0ce47-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="0ce47-125">Un dispositivo puede establecer atributos o metadatos en un almacenamiento mediante una llamada a [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)o [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="0ce47-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="0ce47-126">Tenga en cuenta que no hay ninguna garantía de que se conserve ningún valor establecido, ya que pueden almacenarse en un almacén de archivos externo no persistente, es posible que no se admitan los valores o que el dispositivo no admita las propiedades como grabable.</span><span class="sxs-lookup"><span data-stu-id="0ce47-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="0ce47-127">También puede obtener o establecer metadatos sobre un dispositivo mediante una llamada a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) o [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="0ce47-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="0ce47-128">Hay una tabla independiente de constantes de metadatos de dispositivo que se enumeran al final de las [constantes de metadatos](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0ce47-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="0ce47-129">En la documentación de referencia de cada método se proporcionan ejemplos de uso de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0ce47-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ce47-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ce47-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce47-131">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="0ce47-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="0ce47-132">**Obtener y establecer metadatos y atributos**</span><span class="sxs-lookup"><span data-stu-id="0ce47-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




