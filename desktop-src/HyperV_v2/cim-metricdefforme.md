---
description: Representa una asociación en la que un \_ objeto BaseMetricDefinition de CIM define las métricas de un elemento administrado.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: CIM_MetricDefForME (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911037"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="32e16-103">\_Clase MetricDefForME de CIM</span><span class="sxs-lookup"><span data-stu-id="32e16-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="32e16-104">Representa una asociación en la que un objeto [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) define las métricas de un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="32e16-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32e16-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="32e16-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="32e16-106">Members</span></span>

<span data-ttu-id="32e16-107">La clase **CIM \_ MetricDefForME** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="32e16-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="32e16-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32e16-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32e16-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32e16-109">Properties</span></span>

<span data-ttu-id="32e16-110">La clase **CIM \_ MetricDefForME** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="32e16-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32e16-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="32e16-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e16-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="32e16-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="32e16-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e16-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e16-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="32e16-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="32e16-115">Elemento administrado que está asociado a la definición de la métrica.</span><span class="sxs-lookup"><span data-stu-id="32e16-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="32e16-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="32e16-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e16-117">Tipo de datos: **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="32e16-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="32e16-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e16-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e16-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="32e16-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="32e16-120">La definición de métrica que está asociada al elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="32e16-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="32e16-121">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="32e16-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e16-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32e16-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32e16-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e16-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e16-124">Indica si se va a recopilar la métrica para el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="32e16-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="32e16-125">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="32e16-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="32e16-126">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="32e16-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="32e16-127">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="32e16-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="32e16-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="32e16-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="32e16-129">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="32e16-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="32e16-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="32e16-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="32e16-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e16-131">Requirements</span></span>



| <span data-ttu-id="32e16-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e16-132">Requirement</span></span> | <span data-ttu-id="32e16-133">Value</span><span class="sxs-lookup"><span data-stu-id="32e16-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e16-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e16-134">Minimum supported client</span></span><br/> | <span data-ttu-id="32e16-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="32e16-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="32e16-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e16-136">Minimum supported server</span></span><br/> | <span data-ttu-id="32e16-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32e16-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="32e16-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32e16-138">Namespace</span></span><br/>                | <span data-ttu-id="32e16-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="32e16-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="32e16-140">MOF</span><span class="sxs-lookup"><span data-stu-id="32e16-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e16-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e16-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32e16-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32e16-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e16-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32e16-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32e16-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e16-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="32e16-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

