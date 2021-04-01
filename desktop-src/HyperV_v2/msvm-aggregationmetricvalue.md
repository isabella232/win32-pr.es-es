---
description: Representa el valor de instancia de una métrica definida por una instancia de la \_ clase MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083099"
---
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="dac89-103">MSVM \_ AggregationMetricValue (clase)</span><span class="sxs-lookup"><span data-stu-id="dac89-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="dac89-104">Representa el valor de instancia de una métrica definida por una instancia de la clase [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="dac89-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="dac89-105">Las propiedades heredadas de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) proporcionan el valor de métrica real.</span><span class="sxs-lookup"><span data-stu-id="dac89-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="dac89-106">Las propiedades definidas por esta clase proporcionan información sobre el intervalo sobre el que se aplicó la función de agregación.</span><span class="sxs-lookup"><span data-stu-id="dac89-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="dac89-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dac89-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac89-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dac89-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="dac89-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dac89-109">Members</span></span>

<span data-ttu-id="dac89-110">La clase **MSVM \_ AggregationMetricValue** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dac89-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="dac89-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dac89-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dac89-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dac89-112">Properties</span></span>

<span data-ttu-id="dac89-113">La clase **MSVM \_ AggregationMetricValue** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dac89-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dac89-114">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="dac89-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-115">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dac89-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-117">Representa la duración de tiempo en la que se calculó la agregación.</span><span class="sxs-lookup"><span data-stu-id="dac89-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="dac89-118">El inicio de un intervalo de supervisión sobre el que se aplica la función de agregación se determina restando el **AggregationDuration** de **AggregationTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="dac89-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="dac89-119">Esta propiedad se hereda de **\_ AggregationMetricValue CIM**.</span><span class="sxs-lookup"><span data-stu-id="dac89-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="dac89-120">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="dac89-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-121">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dac89-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-123">Identifica la hora en que se aplicó la función de agregación para determinar el valor de la instancia de métrica.</span><span class="sxs-lookup"><span data-stu-id="dac89-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="dac89-124">Esto no es lo mismo que la hora en que se creó la instancia.</span><span class="sxs-lookup"><span data-stu-id="dac89-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="dac89-125">En el caso de una instancia de **\_ AggregationMetricValue de CIM** determinada, el **AggregationTimeStamp** cambia cada vez que se aplica la función de agregación para calcular el valor.</span><span class="sxs-lookup"><span data-stu-id="dac89-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="dac89-126">Esta propiedad se hereda de **\_ AggregationMetricValue CIM**.</span><span class="sxs-lookup"><span data-stu-id="dac89-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="dac89-127">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="dac89-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-130">Especifica una dimensión de desglose de la matriz **BreakdownDimensions** definida en la [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="dac89-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="dac89-131">Esta es la dimensión en la que se divide este conjunto de valores de métricas.</span><span class="sxs-lookup"><span data-stu-id="dac89-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="dac89-132">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-133">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="dac89-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-136">Define un valor de la propiedad **BreakdownDimension** definida para esta instancia de valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="dac89-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="dac89-137">Por ejemplo, si **BreakdownDimension** es "TransactionName", esta propiedad podría nombrar la transacción real a la que se aplica este valor de métrica en particular.</span><span class="sxs-lookup"><span data-stu-id="dac89-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="dac89-138">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dac89-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="dac89-142">A short description of the object.</span></span> <span data-ttu-id="dac89-143">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dac89-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-147">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="dac89-147">A description of the object.</span></span> <span data-ttu-id="dac89-148">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-149">**Duration**</span><span class="sxs-lookup"><span data-stu-id="dac89-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-150">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dac89-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-152">Especifica la duración de la validez de este valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="dac89-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="dac89-153">Esta propiedad no debe existir para las marcas de tiempo que se aplican solo a un punto en el tiempo, pero debe especificarse para los valores que se consideran válidos para un determinado período de tiempo (por ejemplo, muestreo).</span><span class="sxs-lookup"><span data-stu-id="dac89-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="dac89-154">Si la propiedad **Duration** existe y no es **null**, la propiedad **timestamp** especifica el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="dac89-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="dac89-155">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dac89-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-159">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="dac89-159">A display name for the object.</span></span> <span data-ttu-id="dac89-160">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dac89-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dac89-164">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="dac89-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dac89-165">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="dac89-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dac89-166">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-167">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="dac89-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-170">Un nombre descriptivo para el elemento al que pertenece el valor de métrica (el elemento medido).</span><span class="sxs-lookup"><span data-stu-id="dac89-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="dac89-171">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="dac89-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-175">La clave de la instancia de [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md) para este valor.</span><span class="sxs-lookup"><span data-stu-id="dac89-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="dac89-176">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-177">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="dac89-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dac89-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-180">Valor de la métrica que se representa como una cadena.</span><span class="sxs-lookup"><span data-stu-id="dac89-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="dac89-181">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-182">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="dac89-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-183">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dac89-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-185">Especifica la hora a la que se capturó o calculó el valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="dac89-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="dac89-186">Tenga en cuenta que esto es diferente del momento en que se creó la instancia.</span><span class="sxs-lookup"><span data-stu-id="dac89-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="dac89-187">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dac89-188">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="dac89-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac89-189">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dac89-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dac89-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dac89-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dac89-191">**True** si el valor para el siguiente punto en el tiempo usará la misma instancia de la clase y simplemente cambiará los valores de propiedad (como el **valor** o la **marca** de tiempo).</span><span class="sxs-lookup"><span data-stu-id="dac89-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="dac89-192">Si es **true**, la instancia se reutiliza.</span><span class="sxs-lookup"><span data-stu-id="dac89-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="dac89-193">Si **es false**, las instancias existentes permanecen sin cambios y se crea una nueva instancia para el nuevo punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="dac89-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="dac89-194">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dac89-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dac89-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac89-195">Requirements</span></span>



| <span data-ttu-id="dac89-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac89-196">Requirement</span></span> | <span data-ttu-id="dac89-197">Value</span><span class="sxs-lookup"><span data-stu-id="dac89-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac89-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac89-198">Minimum supported client</span></span><br/> | <span data-ttu-id="dac89-199">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac89-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dac89-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac89-200">Minimum supported server</span></span><br/> | <span data-ttu-id="dac89-201">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac89-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dac89-202">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dac89-202">Namespace</span></span><br/>                | <span data-ttu-id="dac89-203">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dac89-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dac89-204">MOF</span><span class="sxs-lookup"><span data-stu-id="dac89-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dac89-205"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dac89-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dac89-206">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dac89-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dac89-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dac89-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

