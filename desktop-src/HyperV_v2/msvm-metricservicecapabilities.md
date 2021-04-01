---
description: Describe las capacidades de la instancia de MSVM \_ MetricService asociada.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913118"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="38e3d-103">MSVM \_ MetricServiceCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="38e3d-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="38e3d-104">Describe las capacidades de la instancia de [**MSVM \_ MetricService**](msvm-metricservice.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="38e3d-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="38e3d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="38e3d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e3d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38e3d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="38e3d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="38e3d-107">Members</span></span>

<span data-ttu-id="38e3d-108">La clase **MSVM \_ MetricServiceCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="38e3d-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="38e3d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38e3d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38e3d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38e3d-110">Properties</span></span>

<span data-ttu-id="38e3d-111">La clase **MSVM \_ MetricServiceCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="38e3d-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38e3d-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="38e3d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e3d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e3d-115">A short description of the object.</span></span> <span data-ttu-id="38e3d-116">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="38e3d-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="38e3d-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="38e3d-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-120">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="38e3d-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-121">Identifica las instancias de la clase [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que puede controlar la instancia de **\_ MetricService CIM** asociada.</span><span class="sxs-lookup"><span data-stu-id="38e3d-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="38e3d-122">Si esta propiedad es **null**, se pueden controlar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="38e3d-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="38e3d-123">Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="38e3d-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-125">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="38e3d-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-127">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="38e3d-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-128">Identifica las instancias de **\_ BaseMetricDefinition de CIM** que puede controlar la instancia de **\_ MetricService de CIM** asociada.</span><span class="sxs-lookup"><span data-stu-id="38e3d-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="38e3d-129">Si esta propiedad es **null**, se pueden controlar todas las métricas.</span><span class="sxs-lookup"><span data-stu-id="38e3d-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="38e3d-130">Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38e3d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e3d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-134">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e3d-134">A description of the object.</span></span> <span data-ttu-id="38e3d-135">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "define las capacidades del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="38e3d-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="38e3d-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e3d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-139">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e3d-139">A display name for the object.</span></span> <span data-ttu-id="38e3d-140">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="38e3d-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="38e3d-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="38e3d-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-144">Indica si se puede modificar la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="38e3d-145">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="38e3d-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e3d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-149">Especifica las restricciones en **ElementName**, expresadas como una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="38e3d-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="38e3d-150">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="38e3d-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e3d-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-154">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="38e3d-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-155">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="38e3d-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="38e3d-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38e3d-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="38e3d-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-158">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38e3d-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-160">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="38e3d-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-161">Identifica el tipo de control admitido por la instancia de **\_ MetricService CIM** asociada para el objeto [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificado por el valor en el mismo índice de matriz en la propiedad **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="38e3d-162">Si esta propiedad es **null**, se admiten todos los tipos de control.</span><span class="sxs-lookup"><span data-stu-id="38e3d-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="38e3d-163">Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="38e3d-164">Value</span><span class="sxs-lookup"><span data-stu-id="38e3d-164">Value</span></span>                                                                                   | <span data-ttu-id="38e3d-165">Significado</span><span class="sxs-lookup"><span data-stu-id="38e3d-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="38e3d-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="38e3d-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="38e3d-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="38e3d-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="38e3d-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="38e3d-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="38e3d-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="38e3d-171">En bloque</span><span class="sxs-lookup"><span data-stu-id="38e3d-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="38e3d-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="38e3d-173">Ambos</span><span class="sxs-lookup"><span data-stu-id="38e3d-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="38e3d-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="38e3d-175">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="38e3d-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="38e3d-176"><dt>32768... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="38e3d-177">Específico del proveedor</span><span class="sxs-lookup"><span data-stu-id="38e3d-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="38e3d-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="38e3d-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-179">Tipo de datos: **unit16**</span><span class="sxs-lookup"><span data-stu-id="38e3d-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-181">Calificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="38e3d-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-182">Especifica la longitud máxima admitida de la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="38e3d-183">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38e3d-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="38e3d-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-185">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38e3d-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-187">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="38e3d-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-188">Identifica el tipo de control admitido por la instancia de **\_ MetricService CIM** asociada para el **\_ BaseMetricDefinition CIM** identificado por el valor en el mismo índice de matriz en la propiedad **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="38e3d-189">Si esta propiedad es **null**, se admiten todos los tipos de control.</span><span class="sxs-lookup"><span data-stu-id="38e3d-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="38e3d-190">Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="38e3d-191">Value</span><span class="sxs-lookup"><span data-stu-id="38e3d-191">Value</span></span>                                                                                   | <span data-ttu-id="38e3d-192">Significado</span><span class="sxs-lookup"><span data-stu-id="38e3d-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="38e3d-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="38e3d-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="38e3d-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="38e3d-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="38e3d-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="38e3d-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="38e3d-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="38e3d-198">En bloque</span><span class="sxs-lookup"><span data-stu-id="38e3d-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="38e3d-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="38e3d-200">Ambos</span><span class="sxs-lookup"><span data-stu-id="38e3d-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="38e3d-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="38e3d-202">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="38e3d-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="38e3d-203"><dt>32768... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="38e3d-204">Específico del proveedor</span><span class="sxs-lookup"><span data-stu-id="38e3d-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="38e3d-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="38e3d-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-206">Tipo de datos: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="38e3d-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-208">Indica los posibles Estados que se pueden solicitar al utilizar el método **RequestStateChange** en el elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="38e3d-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="38e3d-209">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="38e3d-210">Value</span><span class="sxs-lookup"><span data-stu-id="38e3d-210">Value</span></span>                                                                         | <span data-ttu-id="38e3d-211">Significado</span><span class="sxs-lookup"><span data-stu-id="38e3d-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="38e3d-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="38e3d-213">habilitado</span><span class="sxs-lookup"><span data-stu-id="38e3d-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="38e3d-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="38e3d-215">Impide</span><span class="sxs-lookup"><span data-stu-id="38e3d-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="38e3d-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="38e3d-217">Apagar</span><span class="sxs-lookup"><span data-stu-id="38e3d-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="38e3d-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="38e3d-219">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="38e3d-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="38e3d-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="38e3d-221">Prueba</span><span class="sxs-lookup"><span data-stu-id="38e3d-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="38e3d-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="38e3d-223">Acepta</span><span class="sxs-lookup"><span data-stu-id="38e3d-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="38e3d-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="38e3d-225">Modo de inactividad</span><span class="sxs-lookup"><span data-stu-id="38e3d-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="38e3d-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="38e3d-227">Reboot</span><span class="sxs-lookup"><span data-stu-id="38e3d-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="38e3d-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="38e3d-229">Reset</span><span class="sxs-lookup"><span data-stu-id="38e3d-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="38e3d-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="38e3d-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e3d-231">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38e3d-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38e3d-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e3d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e3d-233">Especifica los métodos admitidos por el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="38e3d-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="38e3d-234">Esta propiedad se hereda de **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="38e3d-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="38e3d-235">Value</span><span class="sxs-lookup"><span data-stu-id="38e3d-235">Value</span></span>                                                                                   | <span data-ttu-id="38e3d-236">Significado</span><span class="sxs-lookup"><span data-stu-id="38e3d-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38e3d-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="38e3d-238">Se admite el método [**ControlMetrics**](controlmetrics-msvm-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="38e3d-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="38e3d-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="38e3d-240">Se admite el método **ControlMetricsByClass** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="38e3d-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="38e3d-242">Se admite el método **ShowMetrics** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="38e3d-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="38e3d-244">Se admite el método **ShowMetricsByClass** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="38e3d-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="38e3d-246">Se admite el método **GetMetricValues** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="38e3d-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="38e3d-248">Se admite el método **ControlSampleTimes** .</span><span class="sxs-lookup"><span data-stu-id="38e3d-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="38e3d-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="38e3d-250">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="38e3d-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="38e3d-251"><dt>32768... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="38e3d-252">Específico del proveedor</span><span class="sxs-lookup"><span data-stu-id="38e3d-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38e3d-253">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e3d-253">Requirements</span></span>



| <span data-ttu-id="38e3d-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e3d-254">Requirement</span></span> | <span data-ttu-id="38e3d-255">Value</span><span class="sxs-lookup"><span data-stu-id="38e3d-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e3d-256">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e3d-256">Minimum supported client</span></span><br/> | <span data-ttu-id="38e3d-257">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="38e3d-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38e3d-258">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e3d-258">Minimum supported server</span></span><br/> | <span data-ttu-id="38e3d-259">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="38e3d-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38e3d-260">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38e3d-260">Namespace</span></span><br/>                | <span data-ttu-id="38e3d-261">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="38e3d-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38e3d-262">MOF</span><span class="sxs-lookup"><span data-stu-id="38e3d-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38e3d-263"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38e3d-264">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38e3d-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38e3d-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38e3d-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38e3d-266">Vea también</span><span class="sxs-lookup"><span data-stu-id="38e3d-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e3d-267">**\_METRICSERVICECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="38e3d-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="38e3d-268">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="38e3d-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

