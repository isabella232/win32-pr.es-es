---
description: La \_ clase CIM ComputerSystemIRQ representa una asociación entre un equipo y sus líneas de solicitud de interrupción (IRQ) disponibles.
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: CIM_ComputerSystemIRQ (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659629"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="03938-103">\_Clase ComputerSystemIRQ de CIM</span><span class="sxs-lookup"><span data-stu-id="03938-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="03938-104">La clase **CIM \_ ComputerSystemIRQ** representa una asociación entre un equipo y sus líneas de solicitud de interrupción (IRQ) disponibles.</span><span class="sxs-lookup"><span data-stu-id="03938-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03938-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="03938-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03938-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03938-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03938-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="03938-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03938-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="03938-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03938-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03938-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="03938-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="03938-110">Members</span></span>

<span data-ttu-id="03938-111">La clase **CIM \_ ComputerSystemIRQ** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03938-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="03938-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03938-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03938-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03938-113">Properties</span></span>

<span data-ttu-id="03938-114">La clase **CIM \_ ComputerSystemIRQ** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03938-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03938-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="03938-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03938-116">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="03938-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="03938-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03938-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03938-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="03938-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="03938-119">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el equipo asociado a la IRQ.</span><span class="sxs-lookup"><span data-stu-id="03938-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="03938-120">Esta propiedad se hereda de [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="03938-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="03938-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="03938-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03938-122">Tipo de datos **: \_ IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="03938-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="03938-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03938-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03938-124">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03938-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03938-125">Una [**\_ IRQ CIM**](cim-irq.md) que describe una IRQ del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="03938-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03938-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03938-126">Remarks</span></span>

<span data-ttu-id="03938-127">La clase **CIM \_ ComputerSystemIRQ** se deriva de [**\_ ComputerSystemResource de CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="03938-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="03938-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="03938-128">WMI does not implement this class.</span></span>

<span data-ttu-id="03938-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="03938-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03938-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="03938-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03938-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03938-131">Requirements</span></span>



| <span data-ttu-id="03938-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="03938-132">Requirement</span></span> | <span data-ttu-id="03938-133">Value</span><span class="sxs-lookup"><span data-stu-id="03938-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03938-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03938-134">Minimum supported client</span></span><br/> | <span data-ttu-id="03938-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03938-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03938-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03938-136">Minimum supported server</span></span><br/> | <span data-ttu-id="03938-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03938-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03938-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03938-138">Namespace</span></span><br/>                | <span data-ttu-id="03938-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="03938-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03938-140">MOF</span><span class="sxs-lookup"><span data-stu-id="03938-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03938-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03938-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03938-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03938-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03938-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03938-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03938-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="03938-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03938-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="03938-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

