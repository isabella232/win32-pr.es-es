---
description: Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668430"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="14284-103">MSVM \_ BasedOn (clase)</span><span class="sxs-lookup"><span data-stu-id="14284-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="14284-104">Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="14284-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="14284-105">Por ejemplo, ProtectedSpaceExtents son partes de PhysicalExtents, mientras que VolumeSets se ensamblan desde uno o varios físicos o ProtectedSpaceExtents.</span><span class="sxs-lookup"><span data-stu-id="14284-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="14284-106">Como otro ejemplo, CacheMemory puede definirse de forma independiente y realizarse en un PhysicalElement o puede basarse en volatile o NonVolatileStorageExtents.</span><span class="sxs-lookup"><span data-stu-id="14284-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="14284-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="14284-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14284-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14284-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="14284-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="14284-109">Members</span></span>

<span data-ttu-id="14284-110">La **clase \_ basada en MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="14284-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="14284-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14284-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14284-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14284-112">Properties</span></span>

<span data-ttu-id="14284-113">La **clase \_ basada en MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="14284-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14284-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="14284-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14284-115">Tipo de datos: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="14284-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="14284-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14284-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14284-117">La extensión de almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="14284-117">The lower level storage extent.</span></span> <span data-ttu-id="14284-118">Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="14284-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="14284-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="14284-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14284-120">Tipo de datos: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="14284-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="14284-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14284-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14284-122">La extensión de almacenamiento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="14284-122">The higher level storage extent.</span></span> <span data-ttu-id="14284-123">Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="14284-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="14284-124">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="14284-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14284-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14284-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14284-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14284-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14284-127">Dirección final en la que finaliza la extensión de nivel superior en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="14284-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="14284-128">Esta propiedad es útil cuando se asignan extensiones no contiguas en una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="14284-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="14284-129">Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="14284-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="14284-130">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="14284-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14284-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14284-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14284-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14284-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14284-133">Si hay un pedido al basado en asociaciones que describen cómo se ensambla una extensión de almacenamiento de nivel superior, la propiedad **OrderIndex** indica esto.</span><span class="sxs-lookup"><span data-stu-id="14284-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="14284-134">Cuando existe un pedido, las instancias con el mismo valor **dependiente** (la misma extensión de nivel superior) deben colocar valores únicos en la propiedad **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="14284-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="14284-135">El valor más bajo implica al primer miembro de la colección de extensiones de nivel inferior y los valores que aumentan implican a miembros sucesivos de la colección.</span><span class="sxs-lookup"><span data-stu-id="14284-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="14284-136">Si no hay ninguna relación ordenada, se debe especificar un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="14284-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="14284-137">Un ejemplo del uso de esta propiedad es definir una matriz seccionada RAID-0 de tres discos.</span><span class="sxs-lookup"><span data-stu-id="14284-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="14284-138">La matriz RAID resultante es una extensión de almacenamiento que depende de las extensiones de almacenamiento que describen cada uno de los tres discos.</span><span class="sxs-lookup"><span data-stu-id="14284-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="14284-139">El **OrderIndex** de cada Asociación de las extensiones de disco a la matriz RAID podría especificarse como 1, 2 y 3 para indicar el orden en que se usan las extensiones de disco para tener acceso a los datos de RAID.</span><span class="sxs-lookup"><span data-stu-id="14284-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="14284-140">Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="14284-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="14284-141">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="14284-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14284-142">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14284-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14284-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14284-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14284-144">La dirección inicial en la que se inicia la extensión de nivel superior en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="14284-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="14284-145">Esta propiedad se hereda de [**\_ BasedOn CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="14284-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14284-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14284-146">Requirements</span></span>



| <span data-ttu-id="14284-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="14284-147">Requirement</span></span> | <span data-ttu-id="14284-148">Value</span><span class="sxs-lookup"><span data-stu-id="14284-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14284-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14284-149">Minimum supported client</span></span><br/> | <span data-ttu-id="14284-150">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="14284-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="14284-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14284-151">Minimum supported server</span></span><br/> | <span data-ttu-id="14284-152">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="14284-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14284-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14284-153">Namespace</span></span><br/>                | <span data-ttu-id="14284-154">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="14284-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="14284-155">MOF</span><span class="sxs-lookup"><span data-stu-id="14284-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14284-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14284-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14284-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14284-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14284-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14284-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

