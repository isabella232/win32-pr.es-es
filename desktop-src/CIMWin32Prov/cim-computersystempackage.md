---
description: La \_ clase CIM ComputerSystemPackage representa una asociación que define explícitamente la relación entre los sistemas de equipos unitarios y uno o varios paquetes físicos.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: CIM_ComputerSystemPackage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000663"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="a348b-103">\_Clase ComputerSystemPackage de CIM</span><span class="sxs-lookup"><span data-stu-id="a348b-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="a348b-104">La clase **CIM \_ ComputerSystemPackage** representa una asociación que define explícitamente la relación entre los sistemas de equipos unitarios y uno o varios paquetes físicos.</span><span class="sxs-lookup"><span data-stu-id="a348b-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="a348b-105">La asociación es similar a la forma en que los dispositivos lógicos se encontraban en los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="a348b-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a348b-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a348b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a348b-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a348b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a348b-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a348b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a348b-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a348b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a348b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a348b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a348b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a348b-111">Members</span></span>

<span data-ttu-id="a348b-112">La clase **CIM \_ ComputerSystemPackage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a348b-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="a348b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a348b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a348b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a348b-114">Properties</span></span>

<span data-ttu-id="a348b-115">La clase **CIM \_ ComputerSystemPackage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a348b-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a348b-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a348b-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a348b-117">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="a348b-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="a348b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a348b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a348b-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="a348b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a348b-120">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe los paquetes físicos que obtienen un sistema de equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="a348b-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a348b-121">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a348b-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a348b-122">Tipo de datos: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a348b-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a348b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a348b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a348b-124">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="a348b-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a348b-125">Un [**\_ UnitaryComputerSystem de CIM**](cim-unitarycomputersystem.md) que describe el sistema del equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="a348b-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a348b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a348b-126">Remarks</span></span>

<span data-ttu-id="a348b-127">La clase **CIM \_ ComputerSystemPackage** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a348b-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a348b-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a348b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="a348b-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a348b-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a348b-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a348b-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a348b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a348b-131">Requirements</span></span>



| <span data-ttu-id="a348b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a348b-132">Requirement</span></span> | <span data-ttu-id="a348b-133">Value</span><span class="sxs-lookup"><span data-stu-id="a348b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a348b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a348b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a348b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a348b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a348b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a348b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a348b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a348b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a348b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a348b-138">Namespace</span></span><br/>                | <span data-ttu-id="a348b-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a348b-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a348b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a348b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a348b-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a348b-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a348b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a348b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a348b-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a348b-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a348b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a348b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a348b-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a348b-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

