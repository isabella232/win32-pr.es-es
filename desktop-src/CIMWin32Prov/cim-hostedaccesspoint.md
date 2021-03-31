---
description: La \_ clase CIM HostedAccessPoint representa una asociación entre un punto de acceso de servicio (SAP) y el sistema en el que se proporciona. Cada sistema puede hospedar muchos SAP.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: CIM_HostedAccessPoint (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153174"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="26159-104">CIM_HostedAccessPoint (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="26159-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="26159-105">La clase **CIM \_ HostedAccessPoint** representa una asociación entre un punto de acceso de servicio (SAP) y el sistema en el que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="26159-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="26159-106">Cada sistema puede hospedar muchos SAP.</span><span class="sxs-lookup"><span data-stu-id="26159-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26159-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="26159-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26159-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26159-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26159-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="26159-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="26159-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="26159-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26159-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26159-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="26159-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="26159-112">Members</span></span>

<span data-ttu-id="26159-113">La clase **CIM \_ HostedAccessPoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="26159-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="26159-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26159-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26159-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26159-115">Properties</span></span>

<span data-ttu-id="26159-116">La clase **CIM \_ HostedAccessPoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="26159-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26159-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="26159-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26159-118">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="26159-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="26159-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26159-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26159-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="26159-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="26159-121">[**\_ Sistema CIM**](cim-system.md) que describe el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="26159-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="26159-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="26159-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26159-123">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="26159-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="26159-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26159-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26159-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26159-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26159-126">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe las SAP que se hospedan en este sistema.</span><span class="sxs-lookup"><span data-stu-id="26159-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26159-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26159-127">Remarks</span></span>

<span data-ttu-id="26159-128">**CIM \_ HostedAccessPoint** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="26159-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="26159-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="26159-129">WMI does not implement this class.</span></span>

<span data-ttu-id="26159-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="26159-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26159-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="26159-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26159-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26159-132">Requirements</span></span>



| <span data-ttu-id="26159-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="26159-133">Requirement</span></span> | <span data-ttu-id="26159-134">Value</span><span class="sxs-lookup"><span data-stu-id="26159-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26159-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26159-135">Minimum supported client</span></span><br/> | <span data-ttu-id="26159-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26159-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26159-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26159-137">Minimum supported server</span></span><br/> | <span data-ttu-id="26159-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26159-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26159-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26159-139">Namespace</span></span><br/>                | <span data-ttu-id="26159-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="26159-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26159-141">MOF</span><span class="sxs-lookup"><span data-stu-id="26159-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26159-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26159-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26159-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26159-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26159-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26159-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26159-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="26159-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26159-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="26159-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

