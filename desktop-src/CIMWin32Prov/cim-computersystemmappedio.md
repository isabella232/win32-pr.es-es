---
description: La \_ clase CIM ComputerSystemMappedIO representa una asociación entre un equipo y sus puertos de e/s asignados a memoria disponibles.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: CIM_ComputerSystemMappedIO (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153240"
---
# <a name="cim_computersystemmappedio-class"></a><span data-ttu-id="9b745-103">\_Clase ComputerSystemMappedIO de CIM</span><span class="sxs-lookup"><span data-stu-id="9b745-103">CIM\_ComputerSystemMappedIO class</span></span>

<span data-ttu-id="9b745-104">La clase **CIM \_ ComputerSystemMappedIO** representa una asociación entre un equipo y sus puertos de e/s asignados a memoria disponibles.</span><span class="sxs-lookup"><span data-stu-id="9b745-104">The **CIM\_ComputerSystemMappedIO** class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b745-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9b745-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b745-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b745-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b745-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b745-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b745-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9b745-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b745-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b745-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9b745-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b745-110">Members</span></span>

<span data-ttu-id="9b745-111">La clase **CIM \_ ComputerSystemMappedIO** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b745-111">The **CIM\_ComputerSystemMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="9b745-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b745-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b745-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b745-113">Properties</span></span>

<span data-ttu-id="9b745-114">La clase **CIM \_ ComputerSystemMappedIO** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b745-114">The **CIM\_ComputerSystemMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b745-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9b745-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b745-116">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="9b745-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9b745-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b745-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b745-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="9b745-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="9b745-119">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el sistema del equipo asignado al puerto de e/s.</span><span class="sxs-lookup"><span data-stu-id="9b745-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system mapped to the I/O port.</span></span>

<span data-ttu-id="9b745-120">Esta propiedad se hereda de [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="9b745-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="9b745-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9b745-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b745-122">Tipo de datos: **CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="9b745-122">Data type: **CIM\_MemoryMappedIO**</span></span>
</dt> <dt>

<span data-ttu-id="9b745-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b745-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b745-124">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b745-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b745-125">Un [**\_ MemoryMappedIO de CIM**](cim-memorymappedio.md) que describe un puerto de e/s asignado a la memoria del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="9b745-125">A [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) that describes a memory mapped I/O port of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b745-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b745-126">Remarks</span></span>

<span data-ttu-id="9b745-127">La clase **CIM \_ ComputerSystemMappedIO** se deriva de [**\_ ComputerSystemResource de CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="9b745-127">The **CIM\_ComputerSystemMappedIO** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="9b745-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9b745-128">WMI does not implement this class.</span></span>

<span data-ttu-id="9b745-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b745-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b745-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9b745-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b745-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b745-131">Requirements</span></span>



| <span data-ttu-id="9b745-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b745-132">Requirement</span></span> | <span data-ttu-id="9b745-133">Value</span><span class="sxs-lookup"><span data-stu-id="9b745-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b745-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b745-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9b745-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b745-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b745-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b745-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9b745-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b745-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b745-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b745-138">Namespace</span></span><br/>                | <span data-ttu-id="9b745-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b745-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b745-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9b745-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b745-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b745-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b745-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b745-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b745-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b745-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b745-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b745-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b745-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="9b745-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

