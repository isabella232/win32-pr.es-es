---
description: La \_ clase CIM ResidesOnExtent representa una asociación entre un sistema de archivos y la extensión de almacenamiento donde se encuentra. Normalmente, un sistema de archivos reside en un disco lógico.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: CIM_ResidesOnExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153513"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="23171-104">\_Clase ResidesOnExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="23171-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="23171-105">La clase **CIM \_ ResidesOnExtent** representa una asociación entre un sistema de archivos y la extensión de almacenamiento donde se encuentra.</span><span class="sxs-lookup"><span data-stu-id="23171-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="23171-106">Normalmente, un sistema de archivos reside en un disco lógico.</span><span class="sxs-lookup"><span data-stu-id="23171-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23171-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="23171-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23171-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23171-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23171-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="23171-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="23171-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="23171-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23171-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23171-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="23171-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="23171-112">Members</span></span>

<span data-ttu-id="23171-113">La clase **CIM \_ ResidesOnExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23171-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="23171-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23171-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23171-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23171-115">Properties</span></span>

<span data-ttu-id="23171-116">La clase **CIM \_ ResidesOnExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23171-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23171-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="23171-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23171-118">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="23171-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="23171-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23171-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23171-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="23171-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="23171-121">Un [**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="23171-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="23171-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="23171-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23171-123">Tipo de datos **: \_ sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="23171-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="23171-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23171-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23171-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="23171-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="23171-126">Un sistema de archivos [**CIM \_**](cim-filesystem.md) que describe el sistema de archivos que se encuentra en la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="23171-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23171-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23171-127">Remarks</span></span>

<span data-ttu-id="23171-128">La clase **CIM \_ ResidesOnExtent** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="23171-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="23171-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="23171-129">WMI does not implement this class.</span></span>

<span data-ttu-id="23171-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="23171-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23171-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="23171-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23171-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23171-132">Requirements</span></span>



| <span data-ttu-id="23171-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="23171-133">Requirement</span></span> | <span data-ttu-id="23171-134">Value</span><span class="sxs-lookup"><span data-stu-id="23171-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23171-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23171-135">Minimum supported client</span></span><br/> | <span data-ttu-id="23171-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23171-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23171-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23171-137">Minimum supported server</span></span><br/> | <span data-ttu-id="23171-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23171-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23171-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23171-139">Namespace</span></span><br/>                | <span data-ttu-id="23171-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="23171-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23171-141">MOF</span><span class="sxs-lookup"><span data-stu-id="23171-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23171-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23171-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23171-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23171-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23171-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23171-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23171-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="23171-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23171-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="23171-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

