---
description: 'VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico. En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objetos auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279307"
---
# <a name="helper-objects"></a><span data-ttu-id="1d5cc-104">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="1d5cc-104">Helper Objects</span></span>

<span data-ttu-id="1d5cc-105">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d5cc-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1d5cc-106">VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="1d5cc-107">En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="1d5cc-108">Objeto de enumeración</span><span class="sxs-lookup"><span data-stu-id="1d5cc-108">Enumeration Object</span></span>

<span data-ttu-id="1d5cc-109">Un objeto de enumeración enumera a través de un conjunto de objetos VDS de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="1d5cc-110">Los objetos pueden ser proveedores, subsistemas, controladores, Lun, complejos de LUN, unidades, paquetes de disco, discos, volúmenes o complejos de volumen.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="1d5cc-111">Los llamadores pueden obtener un puntero a un objeto específico seleccionando el objeto deseado de la enumeración devuelto por el método adecuado.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="1d5cc-112">Para obtener un ejemplo de código, vea [trabajar con objetos de enumeración](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1d5cc-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="1d5cc-113">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="1d5cc-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d5cc-114">Type</span></span>                                              | <span data-ttu-id="1d5cc-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d5cc-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="1d5cc-116">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="1d5cc-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="1d5cc-117">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="1d5cc-118">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="1d5cc-118">Associated enumerations</span></span>                           | <span data-ttu-id="1d5cc-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-119">None.</span></span>                                    |
| <span data-ttu-id="1d5cc-120">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="1d5cc-120">Associated structures</span></span>                             | <span data-ttu-id="1d5cc-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="1d5cc-122">Async (objeto)</span><span class="sxs-lookup"><span data-stu-id="1d5cc-122">Async Object</span></span>

<span data-ttu-id="1d5cc-123">Un objeto asincrónico administra las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="1d5cc-124">Los métodos que inician operaciones asincrónicas devuelven un puntero a una interfaz [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , que permite al llamador cancelar, esperar y consultar el estado de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="1d5cc-125">Las operaciones de VDS de ejecución prolongada tienden a implementarse de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="1d5cc-126">Los programas de proveedores de software básicos y dinámicos implementan métodos asincrónicos de forma coherente para las operaciones de volumen, partición y disco.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="1d5cc-127">Los proveedores de hardware opcionalmente implementan métodos relacionados asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="1d5cc-128">Independientemente de cómo el proveedor implemente el método, la operación debe devolver un puntero a una interfaz [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="1d5cc-129">Para obtener un ejemplo de código, vea [administrar operaciones asincrónicas](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1d5cc-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="1d5cc-130">Entre las operaciones asincrónicas se incluyen:</span><span class="sxs-lookup"><span data-stu-id="1d5cc-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="1d5cc-131">Crear un LUN, un volumen o una partición.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="1d5cc-132">Dar formato a un volumen o partición.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="1d5cc-133">Adición o eliminación de un complejo de LUN o volumen.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="1d5cc-134">Dividir un Plex de volumen.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="1d5cc-135">Ampliación o reducción de un LUN o volumen.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="1d5cc-136">Recuperación de un LUN o volumen.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="1d5cc-137">Limpieza de un disco.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="1d5cc-138">Reemplazar un disco.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-138">Replacing a disk.</span></span>

<span data-ttu-id="1d5cc-139">En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="1d5cc-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d5cc-140">Type</span></span>                                              | <span data-ttu-id="1d5cc-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d5cc-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="1d5cc-142">Interfaces que siempre expone este objeto</span><span class="sxs-lookup"><span data-stu-id="1d5cc-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="1d5cc-143">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="1d5cc-144">Enumeraciones asociadas</span><span class="sxs-lookup"><span data-stu-id="1d5cc-144">Associated enumerations</span></span>                           | <span data-ttu-id="1d5cc-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-145">None.</span></span>                          |
| <span data-ttu-id="1d5cc-146">Estructuras asociadas</span><span class="sxs-lookup"><span data-stu-id="1d5cc-146">Associated structures</span></span>                             | <span data-ttu-id="1d5cc-147">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="1d5cc-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d5cc-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5cc-149">Modelo de objetos de VDS</span><span class="sxs-lookup"><span data-stu-id="1d5cc-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="1d5cc-150">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="1d5cc-151">Trabajar con objetos de enumeración</span><span class="sxs-lookup"><span data-stu-id="1d5cc-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="1d5cc-152">Administrar operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="1d5cc-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
