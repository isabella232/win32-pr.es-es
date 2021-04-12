---
description: Enlace de volúmenes y LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Enlace de volúmenes y LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279714"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="f7211-103">Enlace de volúmenes y LUN</span><span class="sxs-lookup"><span data-stu-id="f7211-103">Volume and LUN Binding</span></span>

<span data-ttu-id="f7211-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f7211-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f7211-105">El enlace es la creación de volúmenes o LUN.</span><span class="sxs-lookup"><span data-stu-id="f7211-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="f7211-106">Los volúmenes se componen de extensiones de disco y LUN se componen de extensiones de unidad.</span><span class="sxs-lookup"><span data-stu-id="f7211-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="f7211-107">El enlace selecciona un conjunto de asignaciones para los recursos físicos y se produce dentro de un subsistema, dentro de un paquete o en ambos.</span><span class="sxs-lookup"><span data-stu-id="f7211-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="f7211-108">Todos los programas de proveedor admiten el enlace parcialmente dirigido a un modelo en el que el autor de la llamada especifica solo los atributos de enlace de interés particular y permite al proveedor elegir el resto.</span><span class="sxs-lookup"><span data-stu-id="f7211-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="f7211-109">Las operaciones en VDS para los volúmenes de enlace y LUN son similares, pero no idénticas.</span><span class="sxs-lookup"><span data-stu-id="f7211-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="f7211-110">Por ejemplo, los proveedores de hardware pueden ofrecer opciones de enlace adicionales.</span><span class="sxs-lookup"><span data-stu-id="f7211-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="f7211-111">VDS admite los siguientes cinco tipos de enlaces de volumen y LUN para las configuraciones dirigidas parcialmente.</span><span class="sxs-lookup"><span data-stu-id="f7211-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="f7211-112">(Los proveedores de hardware pueden y admiten muchos otros enlaces).</span><span class="sxs-lookup"><span data-stu-id="f7211-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="f7211-113">Término</span><span class="sxs-lookup"><span data-stu-id="f7211-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="f7211-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7211-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7211-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span><span class="sxs-lookup"><span data-stu-id="f7211-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="f7211-116">Asignación lineal con una y solo una extensión contigua.</span><span class="sxs-lookup"><span data-stu-id="f7211-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="f7211-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Distribuido</span><span class="sxs-lookup"><span data-stu-id="f7211-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="f7211-118">Asignación lineal con varias extensiones no contiguas en varios discos o unidades.</span><span class="sxs-lookup"><span data-stu-id="f7211-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="f7211-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Seccionado</span><span class="sxs-lookup"><span data-stu-id="f7211-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="f7211-120">Asignación que intercala extensiones de volumen contiguas en varios discos o unidades.</span><span class="sxs-lookup"><span data-stu-id="f7211-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="f7211-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Reflejada</span><span class="sxs-lookup"><span data-stu-id="f7211-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="f7211-122">Asignación que mantiene dos o más copias de datos idénticas.</span><span class="sxs-lookup"><span data-stu-id="f7211-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="f7211-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Seccionado con paridad</span><span class="sxs-lookup"><span data-stu-id="f7211-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="f7211-124">Asignación que distribuye la información de comprobación de paridad en varios discos o unidades.</span><span class="sxs-lookup"><span data-stu-id="f7211-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="f7211-125">Las construcciones de VDS se reflejan, seccionan y seccionan con enlaces de paridad de más de un miembro.</span><span class="sxs-lookup"><span data-stu-id="f7211-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="f7211-126">Por ejemplo, un reflejo doble tiene dos miembros.</span><span class="sxs-lookup"><span data-stu-id="f7211-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="f7211-127">Cada miembro puede ocupar extensiones en más de un disco o unidad.</span><span class="sxs-lookup"><span data-stu-id="f7211-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="f7211-128">VDS concatena las extensiones para formar el miembro y, a continuación, enlaza el volumen o LUN en los miembros.</span><span class="sxs-lookup"><span data-stu-id="f7211-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="f7211-129">Un proveedor puede admitir todos los tipos de enlace o cualquier subconjunto.</span><span class="sxs-lookup"><span data-stu-id="f7211-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="f7211-130">En el modelo de objetos de VDS, cada miembro de un reflejo es un objeto independiente denominado complejo.</span><span class="sxs-lookup"><span data-stu-id="f7211-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="f7211-131">De nuevo, los tipos de volumen y LUN son similares, pero no exactos.</span><span class="sxs-lookup"><span data-stu-id="f7211-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="f7211-132">Para obtener una descripción de los tipos de volumen, consulte el [objeto de volumen](volume-object.md). para los tipos de LUN, consulte el [objeto LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="f7211-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="f7211-133">Los tipos de enlace son no tolerantes a errores o tolerantes a errores.</span><span class="sxs-lookup"><span data-stu-id="f7211-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="f7211-134">Enlace no tolerante a errores</span><span class="sxs-lookup"><span data-stu-id="f7211-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="f7211-135">Los volúmenes y LUN no tolerantes a errores no ofrecen recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="f7211-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="f7211-136">Si se produce un error en uno de los ejes que contribuye a un volumen o LUN no tolerante a errores, se produce un error en todo el volumen o LUN.</span><span class="sxs-lookup"><span data-stu-id="f7211-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="f7211-137">En Exchange para el riesgo de datos, los LUN y volúmenes que no son tolerantes a errores ofrecen un rendimiento de entrada/salida que, por lo general, es superior al de los volúmenes y LUN tolerantes a errores.</span><span class="sxs-lookup"><span data-stu-id="f7211-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="f7211-138">VDS admite los siguientes tres tipos no tolerantes a errores: simple, distribuido y seccionado.</span><span class="sxs-lookup"><span data-stu-id="f7211-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="f7211-139">Simple</span><span class="sxs-lookup"><span data-stu-id="f7211-139">Simple</span></span>

![Diagrama que muestra un tipo simple sin tolerancia a errores con 2 paquetes y 2 subsistemas.](images/vdssimplelunvol.png)

<span data-ttu-id="f7211-141">Distribuido</span><span class="sxs-lookup"><span data-stu-id="f7211-141">Spanned</span></span>

![Diagrama que muestra un tipo distribuido no tolerante a errores con 1 Pack y 1 subsistema.](images/vdsspanlunvol.png)

<span data-ttu-id="f7211-143">Seccionado</span><span class="sxs-lookup"><span data-stu-id="f7211-143">Striped</span></span>

![Diagrama que muestra un tipo no tolerante a errores seccionado con 1 Pack y 1 subsistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="f7211-145">Enlace tolerante a errores</span><span class="sxs-lookup"><span data-stu-id="f7211-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="f7211-146">Los siguientes volúmenes y LUN tolerantes a errores ofrecen recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="f7211-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="f7211-147">Si se produce un error en uno de los ejes que contribuye a un volumen o LUN tolerante a errores, los datos se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="f7211-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="f7211-148">En Exchange para la seguridad de los datos, el rendimiento de entrada/salida de los volúmenes y LUN tolerantes a errores suele ser inferior al de los volúmenes y LUN que no son tolerantes a errores.</span><span class="sxs-lookup"><span data-stu-id="f7211-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="f7211-149">VDS admite dos tipos de tolerancia a errores: reflejado y seccionado con paridad.</span><span class="sxs-lookup"><span data-stu-id="f7211-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="f7211-150">Reflejado (reflejo triple)</span><span class="sxs-lookup"><span data-stu-id="f7211-150">Mirrored (three-way mirror)</span></span>

![Diagrama que muestra un tipo de tolerancia a errores de reflejo (reflejo triple).](images/vdsmirrorlunvol.png)

<span data-ttu-id="f7211-152">Seccionado con paridad</span><span class="sxs-lookup"><span data-stu-id="f7211-152">Striped with parity</span></span>

![Diagrama que muestra un tipo de tolerancia a errores con bandas con paridad.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="f7211-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7211-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7211-155">Información general de configuración</span><span class="sxs-lookup"><span data-stu-id="f7211-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="f7211-156">Objeto de volumen</span><span class="sxs-lookup"><span data-stu-id="f7211-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="f7211-157">Objeto LUN</span><span class="sxs-lookup"><span data-stu-id="f7211-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

