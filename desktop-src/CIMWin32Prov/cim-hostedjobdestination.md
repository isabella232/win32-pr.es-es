---
description: La \_ clase CIM HostedJobDestination representa una asociación entre un destino de trabajo y el sistema en el que reside. Un sistema puede hospedar muchas colas de trabajos. Los destinos del trabajo se aplazan al sistema de hospedaje.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: CIM_HostedJobDestination (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274995"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="2afc3-105">\_Clase HostedJobDestination de CIM</span><span class="sxs-lookup"><span data-stu-id="2afc3-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="2afc3-106">La clase **CIM \_ HostedJobDestination** representa una asociación entre un destino de trabajo y el sistema en el que reside.</span><span class="sxs-lookup"><span data-stu-id="2afc3-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="2afc3-107">Un sistema puede hospedar muchas colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="2afc3-107">A system may host many job queues.</span></span> <span data-ttu-id="2afc3-108">Los destinos del trabajo se aplazan al sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2afc3-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2afc3-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2afc3-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2afc3-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2afc3-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2afc3-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2afc3-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2afc3-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2afc3-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afc3-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2afc3-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2afc3-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="2afc3-114">Members</span></span>

<span data-ttu-id="2afc3-115">La clase **CIM \_ HostedJobDestination** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2afc3-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="2afc3-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2afc3-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2afc3-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2afc3-117">Properties</span></span>

<span data-ttu-id="2afc3-118">La clase **CIM \_ HostedJobDestination** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2afc3-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2afc3-119">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2afc3-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afc3-120">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="2afc3-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="2afc3-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2afc3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2afc3-122">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2afc3-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2afc3-123">[**\_ Sistema CIM**](cim-system.md) que describe el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2afc3-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="2afc3-124">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2afc3-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afc3-125">Tipo de datos: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="2afc3-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="2afc3-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2afc3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2afc3-127">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2afc3-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2afc3-128">Un [**\_ JobDestination de CIM**](cim-jobdestination.md) que describe el destino del trabajo hospedado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2afc3-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2afc3-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2afc3-129">Remarks</span></span>

<span data-ttu-id="2afc3-130">**CIM \_ HostedJobDestination** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2afc3-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2afc3-131">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2afc3-131">WMI does not implement this class.</span></span>

<span data-ttu-id="2afc3-132">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2afc3-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2afc3-133">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2afc3-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afc3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2afc3-134">Requirements</span></span>



| <span data-ttu-id="2afc3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2afc3-135">Requirement</span></span> | <span data-ttu-id="2afc3-136">Value</span><span class="sxs-lookup"><span data-stu-id="2afc3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2afc3-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2afc3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2afc3-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2afc3-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2afc3-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2afc3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2afc3-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2afc3-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2afc3-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2afc3-141">Namespace</span></span><br/>                | <span data-ttu-id="2afc3-142">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2afc3-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2afc3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2afc3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2afc3-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2afc3-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2afc3-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2afc3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2afc3-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2afc3-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2afc3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2afc3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afc3-148">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2afc3-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

