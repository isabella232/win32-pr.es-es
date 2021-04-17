---
description: Describe las capacidades de un \_ objeto MetricService de CIM.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687710"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="cdf4a-103">\_Clase MetricServiceCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="cdf4a-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="cdf4a-104">Describe las capacidades de un [**objeto \_ MetricService de CIM**](cim-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdf4a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="cdf4a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cdf4a-106">Members</span></span>

<span data-ttu-id="cdf4a-107">La clase **CIM \_ MetricServiceCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cdf4a-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="cdf4a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cdf4a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdf4a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cdf4a-109">Properties</span></span>

<span data-ttu-id="cdf4a-110">La clase **CIM \_ MetricServiceCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cdf4a-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdf4a-111">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf4a-112">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cdf4a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-114">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="cdf4a-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="cdf4a-115">Una matriz que contiene los identificadores de las instancias de [**\_ ManagedElement de CIM**](cim-managedelement.md) que están controladas por el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="cdf4a-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="cdf4a-116">Los identificadores deben tener el formato de Web-Based URI de administración empresarial (WBEM).</span><span class="sxs-lookup"><span data-stu-id="cdf4a-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="cdf4a-117">Para usar esta propiedad, el servicio de métricas debe admitir habilitar o deshabilitar al menos una métrica definida para la instancia de **\_ ManagedElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="cdf4a-118">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf4a-119">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cdf4a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-121">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="cdf4a-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="cdf4a-122">Una matriz que contiene los identificadores del [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que define las métricas administradas por el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="cdf4a-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="cdf4a-123">Los identificadores deben tener el formato de Web-Based URI de administración empresarial (WBEM).</span><span class="sxs-lookup"><span data-stu-id="cdf4a-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="cdf4a-124">Para usar esta propiedad, se debe asociar una instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) a una instancia de [**\_ MetricService**](cim-metricservice.md) de CIM a través de la clase [**\_ ServiceAffectsElement de CIM**](cim-serviceaffectselement.md) .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="cdf4a-125">Además, el servicio de métricas debe admitir la habilitación o deshabilitación de al menos una métrica definida por la instancia de **\_ BaseMetricDefinition de CIM** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="cdf4a-126">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf4a-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cdf4a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-129">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")</span><span class="sxs-lookup"><span data-stu-id="cdf4a-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="cdf4a-130">Matriz que indica los tipos de control que admite el servicio de métricas para los elementos administrados de la matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="cdf4a-131">Esta matriz corresponde a la matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="cdf4a-132">Los tipos de control de esta matriz se asocian a las métricas a través de la matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdf4a-133">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="cdf4a-134">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="cdf4a-135">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="cdf4a-136">**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cdf4a-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="cdf4a-138">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdf4a-139">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf4a-140">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cdf4a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-142">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")</span><span class="sxs-lookup"><span data-stu-id="cdf4a-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="cdf4a-143">Una matriz que indica los tipos de control que admite el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="cdf4a-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="cdf4a-144">Esta matriz corresponde a la matriz **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="cdf4a-145">Los tipos de control de esta matriz se asocian a las métricas a través de la matriz **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="cdf4a-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdf4a-146">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="cdf4a-147">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="cdf4a-148">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="cdf4a-149">**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cdf4a-150">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="cdf4a-151">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdf4a-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf4a-153">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cdf4a-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cdf4a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdf4a-155">Una matriz que contiene los nombres de los métodos admitidos por el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="cdf4a-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="cdf4a-156">**ControlMetrics** (2)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="cdf4a-157">**ControlMetricsByClass** (3)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="cdf4a-158">**ShowMetrics** (4)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="cdf4a-159">**ShowMetricsByClass** (5)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="cdf4a-160">**GetMetricValues** (6)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="cdf4a-161">**ControlSampleTimes** (7)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cdf4a-162">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="cdf4a-163">**Específico del proveedor** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="cdf4a-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="cdf4a-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cdf4a-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cdf4a-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdf4a-165">Requirements</span></span>



| <span data-ttu-id="cdf4a-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf4a-166">Requirement</span></span> | <span data-ttu-id="cdf4a-167">Value</span><span class="sxs-lookup"><span data-stu-id="cdf4a-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf4a-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdf4a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf4a-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cdf4a-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cdf4a-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdf4a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf4a-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdf4a-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cdf4a-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cdf4a-172">Namespace</span></span><br/>                | <span data-ttu-id="cdf4a-173">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cdf4a-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cdf4a-174">MOF</span><span class="sxs-lookup"><span data-stu-id="cdf4a-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdf4a-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdf4a-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdf4a-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cdf4a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf4a-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cdf4a-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cdf4a-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdf4a-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf4a-179">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="cdf4a-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

