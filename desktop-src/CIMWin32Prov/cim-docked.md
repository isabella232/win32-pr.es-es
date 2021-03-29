---
description: La \_ Asociación acoplada CIM representa la relación entre dos chasis. Por ejemplo, un portátil (un tipo de chasis) se puede acoplar en una estación de acoplamiento (otro tipo de chasis). Esta relación típica se describe explícitamente.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: CIM_Docked (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807519"
---
# <a name="cim_docked-class"></a><span data-ttu-id="7c363-105">\_Clase acoplada CIM</span><span class="sxs-lookup"><span data-stu-id="7c363-105">CIM\_Docked class</span></span>

<span data-ttu-id="7c363-106">La **Asociación \_ acoplada CIM** representa la relación entre dos chasis.</span><span class="sxs-lookup"><span data-stu-id="7c363-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="7c363-107">Por ejemplo, un portátil (un tipo de chasis) se puede acoplar en una estación de acoplamiento (otro tipo de chasis).</span><span class="sxs-lookup"><span data-stu-id="7c363-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="7c363-108">Esta relación típica se describe explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7c363-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c363-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7c363-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c363-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c363-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c363-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7c363-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c363-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c363-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7c363-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c363-113">Members</span></span>

<span data-ttu-id="7c363-114">La **clase \_ acoplada CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7c363-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="7c363-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c363-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c363-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c363-116">Properties</span></span>

<span data-ttu-id="7c363-117">La **clase \_ acoplada CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7c363-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c363-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7c363-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c363-119">Tipo de datos **: \_ chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="7c363-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="7c363-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c363-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c363-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7c363-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7c363-122">Un [**\_ chasis CIM**](cim-chassis.md) que describe la estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="7c363-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="7c363-123">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="7c363-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c363-124">Tipo de datos **: \_ chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="7c363-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="7c363-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c363-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c363-126">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="7c363-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7c363-127">Un [**\_ chasis CIM**](cim-chassis.md) que describe el equipo portátil acoplado.</span><span class="sxs-lookup"><span data-stu-id="7c363-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c363-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c363-128">Remarks</span></span>

<span data-ttu-id="7c363-129">La **clase \_ acoplada CIM** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7c363-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7c363-130">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7c363-130">WMI does not implement this class.</span></span>

<span data-ttu-id="7c363-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7c363-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c363-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7c363-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c363-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c363-133">Requirements</span></span>



| <span data-ttu-id="7c363-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c363-134">Requirement</span></span> | <span data-ttu-id="7c363-135">Value</span><span class="sxs-lookup"><span data-stu-id="7c363-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c363-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c363-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c363-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c363-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c363-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c363-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c363-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c363-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c363-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c363-140">Namespace</span></span><br/>                | <span data-ttu-id="7c363-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7c363-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c363-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7c363-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c363-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c363-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c363-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c363-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c363-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c363-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c363-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c363-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c363-147">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7c363-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

