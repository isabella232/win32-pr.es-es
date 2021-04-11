---
description: La \_ Asociación JobDestinationJobs de CIM describe dónde se envía un trabajo para su procesamiento (es decir, a qué destino del trabajo).
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: CIM_JobDestinationJobs (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274991"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="605e9-103">\_Clase JobDestinationJobs de CIM</span><span class="sxs-lookup"><span data-stu-id="605e9-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="605e9-104">La **Asociación \_ JobDestinationJobs de CIM** describe dónde se envía un trabajo para su procesamiento (es decir, a qué destino del trabajo).</span><span class="sxs-lookup"><span data-stu-id="605e9-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="605e9-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="605e9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="605e9-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="605e9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="605e9-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="605e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="605e9-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="605e9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="605e9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="605e9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="605e9-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="605e9-110">Members</span></span>

<span data-ttu-id="605e9-111">La clase **CIM \_ JobDestinationJobs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="605e9-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="605e9-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="605e9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="605e9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="605e9-113">Properties</span></span>

<span data-ttu-id="605e9-114">La clase **CIM \_ JobDestinationJobs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="605e9-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="605e9-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="605e9-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="605e9-116">Tipo de datos: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="605e9-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="605e9-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="605e9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="605e9-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="605e9-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="605e9-119">Un [**\_ JobDestination de CIM**](cim-jobdestination.md) que describe el destino del trabajo, posiblemente una cola.</span><span class="sxs-lookup"><span data-stu-id="605e9-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="605e9-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="605e9-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="605e9-121">Tipo de datos **: \_ trabajo CIM**</span><span class="sxs-lookup"><span data-stu-id="605e9-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="605e9-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="605e9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="605e9-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="605e9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="605e9-124">Un [**\_ trabajo de CIM**](cim-job.md) que describe el trabajo que se encuentra en la cola de trabajos o en el destino.</span><span class="sxs-lookup"><span data-stu-id="605e9-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="605e9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="605e9-125">Remarks</span></span>

<span data-ttu-id="605e9-126">**CIM \_ JobDestinationJobs** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="605e9-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="605e9-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="605e9-127">WMI does not implement this class.</span></span>

<span data-ttu-id="605e9-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="605e9-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="605e9-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="605e9-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="605e9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605e9-130">Requirements</span></span>



| <span data-ttu-id="605e9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="605e9-131">Requirement</span></span> | <span data-ttu-id="605e9-132">Value</span><span class="sxs-lookup"><span data-stu-id="605e9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="605e9-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605e9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="605e9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="605e9-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="605e9-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="605e9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="605e9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="605e9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="605e9-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="605e9-137">Namespace</span></span><br/>                | <span data-ttu-id="605e9-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="605e9-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="605e9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="605e9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="605e9-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="605e9-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="605e9-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="605e9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605e9-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="605e9-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605e9-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="605e9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605e9-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="605e9-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

