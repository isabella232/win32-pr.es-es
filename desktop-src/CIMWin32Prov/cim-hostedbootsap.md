---
description: La \_ clase CIM HostedBootSAP define el sistema de equipo unitario de hospedaje para una \_ clase BOOTSAP de CIM.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000616"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="97016-103">\_Clase HostedBootSAP de CIM</span><span class="sxs-lookup"><span data-stu-id="97016-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="97016-104">La clase **CIM \_ HostedBootSAP** define el sistema de equipo unitario de hospedaje para una clase [**\_ BootSAP de CIM**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="97016-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="97016-105">Puesto que esta relación se subclase de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y de nomenclatura definido para [**\_ punto de CIM**](cim-serviceaccesspoint.md), donde un punto de acceso se pospone a su sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="97016-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="97016-106">En este caso, **\_ BootSAP CIM** debe diferir a su [**clase \_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="97016-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97016-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="97016-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97016-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97016-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97016-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="97016-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="97016-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="97016-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97016-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97016-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="97016-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="97016-112">Members</span></span>

<span data-ttu-id="97016-113">La clase **CIM \_ HostedBootSAP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97016-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="97016-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97016-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97016-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97016-115">Properties</span></span>

<span data-ttu-id="97016-116">La clase **CIM \_ HostedBootSAP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="97016-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97016-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="97016-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97016-118">Tipo de datos: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="97016-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="97016-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97016-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97016-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="97016-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="97016-121">Un [**\_ UnitaryComputerSystem de CIM**](cim-unitarycomputersystem.md) que describe el sistema del equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="97016-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="97016-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="97016-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97016-123">Tipo de datos: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="97016-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="97016-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97016-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97016-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="97016-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="97016-126">Un [**\_ BootSAP de CIM**](cim-bootsap.md) que describe el SAP de arranque hospedado en el sistema del equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="97016-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97016-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97016-127">Remarks</span></span>

<span data-ttu-id="97016-128">La clase **CIM \_ HostedBootSAP** se deriva de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="97016-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="97016-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="97016-129">WMI does not implement this class.</span></span>

<span data-ttu-id="97016-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="97016-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97016-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="97016-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97016-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97016-132">Requirements</span></span>



| <span data-ttu-id="97016-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="97016-133">Requirement</span></span> | <span data-ttu-id="97016-134">Value</span><span class="sxs-lookup"><span data-stu-id="97016-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97016-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97016-135">Minimum supported client</span></span><br/> | <span data-ttu-id="97016-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97016-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97016-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97016-137">Minimum supported server</span></span><br/> | <span data-ttu-id="97016-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97016-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97016-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97016-139">Namespace</span></span><br/>                | <span data-ttu-id="97016-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="97016-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97016-141">MOF</span><span class="sxs-lookup"><span data-stu-id="97016-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97016-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97016-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97016-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97016-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97016-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97016-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97016-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="97016-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97016-146">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="97016-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

