---
description: La \_ clase CIM ClusterServiceAccessBySAP representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: CIM_ClusterServiceAccessBySAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000668"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="3e83c-103">\_Clase ClusterServiceAccessBySAP de CIM</span><span class="sxs-lookup"><span data-stu-id="3e83c-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="3e83c-104">La clase **CIM \_ ClusterServiceAccessBySAP** representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.</span><span class="sxs-lookup"><span data-stu-id="3e83c-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e83c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e83c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e83c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e83c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e83c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3e83c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e83c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3e83c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e83c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e83c-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3e83c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e83c-110">Members</span></span>

<span data-ttu-id="3e83c-111">La clase **CIM \_ ClusterServiceAccessBySAP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e83c-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="3e83c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e83c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e83c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e83c-113">Properties</span></span>

<span data-ttu-id="3e83c-114">La clase **CIM \_ ClusterServiceAccessBySAP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e83c-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e83c-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3e83c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e83c-116">Tipo de datos: **CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="3e83c-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="3e83c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e83c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e83c-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3e83c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3e83c-119">Un [**\_ ClusteringService de CIM**](cim-clusteringservice.md) que describe el servicio de agrupación en clústeres.</span><span class="sxs-lookup"><span data-stu-id="3e83c-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="3e83c-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3e83c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e83c-121">Tipo de datos: **CIM \_ ClusteringSAP**</span><span class="sxs-lookup"><span data-stu-id="3e83c-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="3e83c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e83c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e83c-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="3e83c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3e83c-124">Un [**\_ ClusteringSAP de CIM**](cim-clusteringsap.md) que describe un punto de acceso para el servicio de agrupación en clústeres.</span><span class="sxs-lookup"><span data-stu-id="3e83c-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e83c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e83c-125">Remarks</span></span>

<span data-ttu-id="3e83c-126">La clase **CIM \_ ClusterServiceAccessBySAP** se deriva de [**\_ ServiceAccessBySAP de CIM**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="3e83c-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="3e83c-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3e83c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3e83c-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3e83c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e83c-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3e83c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e83c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e83c-130">Requirements</span></span>



| <span data-ttu-id="3e83c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e83c-131">Requirement</span></span> | <span data-ttu-id="3e83c-132">Value</span><span class="sxs-lookup"><span data-stu-id="3e83c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e83c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e83c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3e83c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e83c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e83c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e83c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3e83c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e83c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e83c-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e83c-137">Namespace</span></span><br/>                | <span data-ttu-id="3e83c-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e83c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e83c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3e83c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e83c-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e83c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e83c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e83c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e83c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e83c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e83c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e83c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e83c-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3e83c-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

