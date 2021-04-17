---
description: La \_ clase CIM HostedService representa una asociación entre un servicio y el sistema en el que reside la funcionalidad.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: CIM_HostedService (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659595"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="0b5d5-103">CIM_HostedService (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0b5d5-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0b5d5-104">La clase **CIM \_ HostedService** representa una asociación entre un servicio y el sistema en el que reside la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="0b5d5-105">Un sistema puede hospedar muchos servicios, que aplazan el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="0b5d5-106">El modelo no representa servicios hospedados en varios sistemas.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b5d5-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b5d5-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b5d5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b5d5-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b5d5-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b5d5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b5d5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0b5d5-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b5d5-112">Members</span></span>

<span data-ttu-id="0b5d5-113">La clase **CIM \_ HostedService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b5d5-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="0b5d5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b5d5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b5d5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b5d5-115">Properties</span></span>

<span data-ttu-id="0b5d5-116">La clase **CIM \_ HostedService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b5d5-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0b5d5-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5d5-118">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="0b5d5-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="0b5d5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b5d5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b5d5-120">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="0b5d5-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0b5d5-121">[**\_ Sistema CIM**](cim-system.md) que describe el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="0b5d5-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0b5d5-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5d5-123">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="0b5d5-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0b5d5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b5d5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b5d5-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b5d5-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b5d5-126">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio hospedado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b5d5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b5d5-127">Remarks</span></span>

<span data-ttu-id="0b5d5-128">**CIM \_ HostedService** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0b5d5-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0b5d5-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-129">WMI does not implement this class.</span></span>

<span data-ttu-id="0b5d5-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b5d5-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b5d5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b5d5-132">Requirements</span></span>



| <span data-ttu-id="0b5d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b5d5-133">Requirement</span></span> | <span data-ttu-id="0b5d5-134">Value</span><span class="sxs-lookup"><span data-stu-id="0b5d5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5d5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b5d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5d5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b5d5-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b5d5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b5d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5d5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b5d5-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b5d5-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b5d5-139">Namespace</span></span><br/>                | <span data-ttu-id="0b5d5-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b5d5-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b5d5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0b5d5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b5d5-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b5d5-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b5d5-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b5d5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b5d5-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b5d5-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b5d5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b5d5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b5d5-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0b5d5-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

