---
description: La \_ clase HostedBootService de CIM asocia un sistema de hospedaje y un servicio de arranque. Puesto que esta relación se ha subclase de CIM \_ HostedService, hereda el esquema de ámbito y de nomenclatura definido para el servicio, donde un servicio se pospone a su sistema de hospedaje.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: CIM_HostedBootService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153172"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="77aa6-104">\_Clase HostedBootService de CIM</span><span class="sxs-lookup"><span data-stu-id="77aa6-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="77aa6-105">La **clase \_ HostedBootService de CIM** asocia un sistema de hospedaje y un servicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="77aa6-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="77aa6-106">Puesto que esta relación se ha subclase de [**CIM \_ HostedService**](cim-hostedservice.md), hereda el esquema de ámbito y de nomenclatura definido para el servicio, donde un servicio se pospone a su sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="77aa6-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77aa6-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="77aa6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="77aa6-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="77aa6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="77aa6-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="77aa6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="77aa6-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="77aa6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77aa6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77aa6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="77aa6-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="77aa6-112">Members</span></span>

<span data-ttu-id="77aa6-113">La clase **CIM \_ HostedBootService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="77aa6-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="77aa6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77aa6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77aa6-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77aa6-115">Properties</span></span>

<span data-ttu-id="77aa6-116">La clase **CIM \_ HostedBootService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="77aa6-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77aa6-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="77aa6-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77aa6-118">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="77aa6-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="77aa6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77aa6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77aa6-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (antecedente)</span><span class="sxs-lookup"><span data-stu-id="77aa6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="77aa6-121">[**\_ Sistema CIM**](cim-system.md) que describe el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="77aa6-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="77aa6-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="77aa6-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77aa6-123">Tipo de datos: **CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="77aa6-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="77aa6-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77aa6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77aa6-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="77aa6-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="77aa6-126">Un [**\_ BootService de CIM**](cim-bootservice.md) que describe el servicio de arranque hospedado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="77aa6-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77aa6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77aa6-127">Remarks</span></span>

<span data-ttu-id="77aa6-128">La clase **CIM \_ HostedBootService** se deriva de [**CIM \_ HostedService**](cim-hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="77aa6-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="77aa6-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="77aa6-129">WMI does not implement this class.</span></span>

<span data-ttu-id="77aa6-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="77aa6-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="77aa6-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="77aa6-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="77aa6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77aa6-132">Requirements</span></span>



| <span data-ttu-id="77aa6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="77aa6-133">Requirement</span></span> | <span data-ttu-id="77aa6-134">Value</span><span class="sxs-lookup"><span data-stu-id="77aa6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77aa6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77aa6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="77aa6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77aa6-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77aa6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77aa6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="77aa6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77aa6-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77aa6-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77aa6-139">Namespace</span></span><br/>                | <span data-ttu-id="77aa6-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="77aa6-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77aa6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="77aa6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77aa6-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77aa6-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77aa6-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77aa6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77aa6-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77aa6-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77aa6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="77aa6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77aa6-146">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="77aa6-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

