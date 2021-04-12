---
description: La \_ Asociación RelatedStatistics de CIM representa jerarquías y dependencias de \_ las clases de StatisticalInformation CIM relacionadas.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: CIM_RelatedStatistics (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538488"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="9b331-103">\_Clase RelatedStatistics de CIM</span><span class="sxs-lookup"><span data-stu-id="9b331-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="9b331-104">La **Asociación \_ RelatedStatistics de CIM** representa jerarquías y dependencias de las clases de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9b331-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b331-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9b331-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b331-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b331-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b331-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b331-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b331-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9b331-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b331-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b331-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="9b331-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b331-110">Members</span></span>

<span data-ttu-id="9b331-111">La clase **CIM \_ RelatedStatistics** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b331-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="9b331-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b331-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b331-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b331-113">Properties</span></span>

<span data-ttu-id="9b331-114">La clase **CIM \_ RelatedStatistics** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b331-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b331-115">**RelatedStats**</span><span class="sxs-lookup"><span data-stu-id="9b331-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b331-116">Tipo de datos: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="9b331-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="9b331-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b331-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b331-118">Referencia a las estadísticas o métricas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9b331-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="9b331-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="9b331-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b331-120">Tipo de datos: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="9b331-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="9b331-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b331-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b331-122">Referencia a la información u objeto de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="9b331-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b331-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b331-123">Remarks</span></span>

<span data-ttu-id="9b331-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9b331-124">WMI does not implement this class.</span></span>

<span data-ttu-id="9b331-125">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b331-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b331-126">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9b331-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b331-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b331-127">Requirements</span></span>



| <span data-ttu-id="9b331-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b331-128">Requirement</span></span> | <span data-ttu-id="9b331-129">Value</span><span class="sxs-lookup"><span data-stu-id="9b331-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b331-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b331-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9b331-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b331-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b331-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b331-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9b331-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b331-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b331-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b331-134">Namespace</span></span><br/>                | <span data-ttu-id="9b331-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b331-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b331-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9b331-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b331-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b331-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b331-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b331-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b331-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b331-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




