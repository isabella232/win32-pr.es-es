---
description: La \_ clase MemoryWithMedia de CIM asocia la memoria física con un medio físico y su cartucho. La memoria proporciona identificación de medios y almacena datos específicos del usuario.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: CIM_MemoryWithMedia (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361926"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="472e6-104">\_Clase MemoryWithMedia de CIM</span><span class="sxs-lookup"><span data-stu-id="472e6-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="472e6-105">La **clase \_ MemoryWithMedia de CIM** asocia la memoria física con un medio físico y su cartucho.</span><span class="sxs-lookup"><span data-stu-id="472e6-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="472e6-106">La memoria proporciona identificación de medios y almacena datos específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="472e6-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="472e6-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="472e6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="472e6-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="472e6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="472e6-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="472e6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="472e6-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="472e6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="472e6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="472e6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="472e6-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="472e6-112">Members</span></span>

<span data-ttu-id="472e6-113">La clase **CIM \_ MemoryWithMedia** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="472e6-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="472e6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="472e6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="472e6-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="472e6-115">Properties</span></span>

<span data-ttu-id="472e6-116">La clase **CIM \_ MemoryWithMedia** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="472e6-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="472e6-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="472e6-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="472e6-118">Tipo de datos: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="472e6-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="472e6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="472e6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="472e6-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="472e6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="472e6-121">Un [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) que describe la memoria asociada a un medio físico.</span><span class="sxs-lookup"><span data-stu-id="472e6-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="472e6-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="472e6-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="472e6-123">Tipo de datos: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="472e6-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="472e6-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="472e6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="472e6-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="472e6-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="472e6-126">Un [**\_ PhysicalMedia de CIM**](cim-physicalmedia.md) que describe el medio físico.</span><span class="sxs-lookup"><span data-stu-id="472e6-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="472e6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="472e6-127">Remarks</span></span>

<span data-ttu-id="472e6-128">**CIM \_ MemoryWithMedia** se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="472e6-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="472e6-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="472e6-129">WMI does not implement this class.</span></span>

<span data-ttu-id="472e6-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="472e6-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="472e6-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="472e6-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="472e6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472e6-132">Requirements</span></span>



| <span data-ttu-id="472e6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="472e6-133">Requirement</span></span> | <span data-ttu-id="472e6-134">Value</span><span class="sxs-lookup"><span data-stu-id="472e6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="472e6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="472e6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="472e6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="472e6-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="472e6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="472e6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="472e6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="472e6-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="472e6-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="472e6-139">Namespace</span></span><br/>                | <span data-ttu-id="472e6-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="472e6-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="472e6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="472e6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="472e6-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="472e6-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="472e6-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="472e6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="472e6-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="472e6-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472e6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="472e6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472e6-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="472e6-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

