---
description: Representa una asociación entre un objeto StorageExtent CIM de nivel superior \_ y un objeto STORAGEEXTENT CIM de nivel inferior \_ . Por ejemplo, un \_ objeto de CIM ProtectedSpaceExtent forma parte de un \_ objeto PHYSICALEXTENT de CIM.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: CIM_BasedOn (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907898"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="b9ebc-104">CIM_BasedOn (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b9ebc-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="b9ebc-105">Representa una asociación entre un objeto **\_ StorageExtent CIM** de nivel superior y un objeto **\_ StorageExtent CIM** de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="b9ebc-106">Por ejemplo, un objeto de [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) forma parte de un objeto [**\_ PhysicalExtent de CIM**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .</span><span class="sxs-lookup"><span data-stu-id="b9ebc-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ebc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9ebc-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="b9ebc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9ebc-108">Members</span></span>

<span data-ttu-id="b9ebc-109">La **clase \_ basada en CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b9ebc-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="b9ebc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9ebc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9ebc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9ebc-111">Properties</span></span>

<span data-ttu-id="b9ebc-112">La **clase \_ basada en CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9ebc-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ebc-114">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9ebc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b9ebc-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b9ebc-117">Objeto StorageExtent de **CIM \_** de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b9ebc-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ebc-119">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9ebc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="b9ebc-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b9ebc-122">Objeto StorageExtent de **CIM \_** de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b9ebc-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ebc-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9ebc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9ebc-126">La dirección que indica en qué lugar de almacenamiento de nivel inferior se termina el objeto **\_ StorageExtent CIM** de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="b9ebc-127">Esta propiedad es útil cuando se asignan objetos **\_ StorageExtent CIM** no contiguos en una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="b9ebc-128">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ebc-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9ebc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9ebc-131">Índice que se usa para especificar el orden de las **asociaciones \_ basadas en CIM** en una colección; de lo contrario, "0" indica que no hay orden.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="b9ebc-132">**CIM \_** Las instancias basadas en con el mismo valor dependiente deben colocar valores únicos en la propiedad **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="b9ebc-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="b9ebc-133">El valor de **OrderIndex** más bajo especifica el primer miembro de la colección.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="b9ebc-134">Un ejemplo del uso de esta propiedad es definir una matriz seccionada RAID-0 de 3 discos.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="b9ebc-135">La matriz RAID resultante es una extensión de almacenamiento que depende de las extensiones de almacenamiento que describen cada uno de los tres discos.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="b9ebc-136">El valor **OrderIndex** de cada **Asociación \_ basada en CIM** de las extensiones de disco a la matriz RAID podría especificarse como 1, 2 y 3 para indicar el orden en el que se usan las extensiones de disco para tener acceso a los datos de RAID.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="b9ebc-137">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9ebc-138">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9ebc-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9ebc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9ebc-140">La dirección que indica en qué lugar de almacenamiento de nivel inferior se inicia el objeto **\_ StorageExtent CIM** de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b9ebc-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9ebc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ebc-141">Requirements</span></span>



| <span data-ttu-id="b9ebc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ebc-142">Requirement</span></span> | <span data-ttu-id="b9ebc-143">Value</span><span class="sxs-lookup"><span data-stu-id="b9ebc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ebc-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ebc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ebc-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b9ebc-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b9ebc-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9ebc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ebc-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9ebc-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b9ebc-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9ebc-148">Namespace</span></span><br/>                | <span data-ttu-id="b9ebc-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b9ebc-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b9ebc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b9ebc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9ebc-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9ebc-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9ebc-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9ebc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9ebc-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9ebc-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9ebc-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ebc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ebc-155">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b9ebc-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

