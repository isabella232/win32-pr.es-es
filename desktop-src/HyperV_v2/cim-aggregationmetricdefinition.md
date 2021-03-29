---
description: Representa la definición de una métrica que se deriva de otro valor de métrica. Un \_ objeto AggregationMetricDefinition de CIM se debe asociar a los objetos de ManagedElement de CIM \_ a los que se aplica.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: CIM_AggregationMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812734"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="275d6-104">\_Clase AggregationMetricDefinition de CIM</span><span class="sxs-lookup"><span data-stu-id="275d6-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="275d6-105">Representa la definición de una métrica que se deriva de otro valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="275d6-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="275d6-106">Un **objeto \_ AggregationMetricDefinition de CIM** se debe asociar a los objetos de **\_ ManagedElement de CIM** a los que se aplica.</span><span class="sxs-lookup"><span data-stu-id="275d6-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="275d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="275d6-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="275d6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="275d6-108">Members</span></span>

<span data-ttu-id="275d6-109">La clase **CIM \_ AggregationMetricDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="275d6-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="275d6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="275d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="275d6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="275d6-111">Properties</span></span>

<span data-ttu-id="275d6-112">La clase **CIM \_ AggregationMetricDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="275d6-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="275d6-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="275d6-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="275d6-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="275d6-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="275d6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="275d6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="275d6-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricDefinition**.**IsContinuous**")</span><span class="sxs-lookup"><span data-stu-id="275d6-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="275d6-117">Indica cómo cambia el valor de métrica mediante atributos comunes como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.</span><span class="sxs-lookup"><span data-stu-id="275d6-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="275d6-118">**Función simple** (5)</span><span class="sxs-lookup"><span data-stu-id="275d6-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="275d6-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="275d6-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="275d6-120">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="275d6-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="275d6-121">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="275d6-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="275d6-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="275d6-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="275d6-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="275d6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="275d6-124">Cálculo básico realizado en una métrica subyacente para llegar al valor de esta métrica derivada.</span><span class="sxs-lookup"><span data-stu-id="275d6-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="275d6-125">Esta propiedad es **null** cuando la propiedad **ChangeType** tiene un valor distinto de "5" (función simple).</span><span class="sxs-lookup"><span data-stu-id="275d6-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="275d6-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="275d6-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="275d6-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="275d6-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="275d6-128">La métrica informa del valor más bajo detectado para la entidad supervisada asociada.</span><span class="sxs-lookup"><span data-stu-id="275d6-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="275d6-129">Esto también se conoce como límite inferior.</span><span class="sxs-lookup"><span data-stu-id="275d6-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="275d6-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="275d6-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="275d6-131">La métrica informa del valor máximo detectado para la entidad supervisada asociada.</span><span class="sxs-lookup"><span data-stu-id="275d6-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="275d6-132">Esto también se conoce como límite máximo.</span><span class="sxs-lookup"><span data-stu-id="275d6-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="275d6-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Promedio** (4)</span><span class="sxs-lookup"><span data-stu-id="275d6-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="275d6-134">La métrica informa del valor promedio de los valores de métricas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="275d6-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="275d6-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)</span><span class="sxs-lookup"><span data-stu-id="275d6-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="275d6-136">La métrica informa del valor medio de los valores de métricas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="275d6-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="275d6-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo** (6)</span><span class="sxs-lookup"><span data-stu-id="275d6-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="275d6-138">la métrica informa del valor modal de los valores de métricas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="275d6-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="275d6-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="275d6-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="275d6-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="275d6-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="275d6-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="275d6-141">Requirements</span></span>



| <span data-ttu-id="275d6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="275d6-142">Requirement</span></span> | <span data-ttu-id="275d6-143">Value</span><span class="sxs-lookup"><span data-stu-id="275d6-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="275d6-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="275d6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="275d6-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="275d6-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="275d6-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="275d6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="275d6-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="275d6-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="275d6-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="275d6-148">Namespace</span></span><br/>                | <span data-ttu-id="275d6-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="275d6-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="275d6-150">MOF</span><span class="sxs-lookup"><span data-stu-id="275d6-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="275d6-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="275d6-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="275d6-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="275d6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="275d6-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="275d6-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="275d6-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="275d6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="275d6-155">**\_BASEMETRICDEFINITION CIM**</span><span class="sxs-lookup"><span data-stu-id="275d6-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 

