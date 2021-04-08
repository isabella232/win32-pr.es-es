---
description: La \_ clase CIM ComputerSystemResource representa una asociación entre un equipo y sus recursos del sistema disponibles.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: CIM_ComputerSystemResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080227"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="6bb9c-103">\_Clase ComputerSystemResource de CIM</span><span class="sxs-lookup"><span data-stu-id="6bb9c-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="6bb9c-104">La clase **CIM \_ ComputerSystemResource** representa una asociación entre un equipo y sus recursos del sistema disponibles.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bb9c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6bb9c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6bb9c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6bb9c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6bb9c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb9c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bb9c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="6bb9c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6bb9c-110">Members</span></span>

<span data-ttu-id="6bb9c-111">La clase **CIM \_ ComputerSystemResource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6bb9c-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6bb9c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6bb9c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bb9c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6bb9c-113">Properties</span></span>

<span data-ttu-id="6bb9c-114">La clase **CIM \_ ComputerSystemResource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6bb9c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb9c-116">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6bb9c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6bb9c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb9c-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6bb9c-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6bb9c-119">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6bb9c-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb9c-121">Tipo de datos: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="6bb9c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6bb9c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb9c-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6bb9c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6bb9c-124">Un [**\_ SystemResource de CIM**](cim-systemresource.md) que describe un recurso del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bb9c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bb9c-125">Remarks</span></span>

<span data-ttu-id="6bb9c-126">La clase **CIM \_ ComputerSystemResource** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6bb9c-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="6bb9c-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-127">WMI does not implement this class.</span></span> <span data-ttu-id="6bb9c-128">Para obtener más información sobre las clases derivadas de **CIM \_ ComputerSystemResource**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6bb9c-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6bb9c-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6bb9c-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6bb9c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb9c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb9c-131">Requirements</span></span>



| <span data-ttu-id="6bb9c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb9c-132">Requirement</span></span> | <span data-ttu-id="6bb9c-133">Value</span><span class="sxs-lookup"><span data-stu-id="6bb9c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb9c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bb9c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb9c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bb9c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6bb9c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bb9c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb9c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bb9c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6bb9c-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6bb9c-138">Namespace</span></span><br/>                | <span data-ttu-id="6bb9c-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6bb9c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6bb9c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6bb9c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bb9c-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bb9c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bb9c-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6bb9c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb9c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb9c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb9c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bb9c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb9c-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6bb9c-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

