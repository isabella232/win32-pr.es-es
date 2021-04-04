---
description: Representa los aspectos de la definición de una métrica que se deriva de otro valor de métrica.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Msvm_AggregationMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277989"
---
# <a name="msvm_aggregationmetricdefinition-class"></a><span data-ttu-id="4466e-103">MSVM \_ AggregationMetricDefinition (clase)</span><span class="sxs-lookup"><span data-stu-id="4466e-103">Msvm\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="4466e-104">Representa los aspectos de la definición de una métrica que se deriva de otro valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="4466e-104">Represents the definition aspects of a metric that is derived from another metric value.</span></span> <span data-ttu-id="4466e-105">El **objeto \_ AggregationMetricDefinition de MSVM** debe estar asociado a los elementos administrados a los que se aplica.</span><span class="sxs-lookup"><span data-stu-id="4466e-105">The **Msvm\_AggregationMetricDefinition** object should be associated with the managed elements to which it applies.</span></span>

<span data-ttu-id="4466e-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4466e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4466e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4466e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="4466e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4466e-108">Members</span></span>

<span data-ttu-id="4466e-109">La clase **MSVM \_ AggregationMetricDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4466e-109">The **Msvm\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="4466e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4466e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4466e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4466e-111">Properties</span></span>

<span data-ttu-id="4466e-112">La clase **MSVM \_ AggregationMetricDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4466e-112">The **Msvm\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4466e-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="4466e-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4466e-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4466e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-116">Define una o más cadenas que se pueden usar para refinar (dividir) las consultas con los valores de métrica a lo largo de una dimensión determinada.</span><span class="sxs-lookup"><span data-stu-id="4466e-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="4466e-117">Un ejemplo es un nombre de transacción, lo que permite el desglose del valor total de todas las transacciones en un conjunto de valores, uno para cada nombre de transacción.</span><span class="sxs-lookup"><span data-stu-id="4466e-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="4466e-118">Otros ejemplos podrían ser sistema de aplicaciones o nombre de grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="4466e-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="4466e-119">Las cadenas tienen un formato libre y deben ser significativas para los usuarios finales de los datos de métricas.</span><span class="sxs-lookup"><span data-stu-id="4466e-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="4466e-120">Las cadenas indican qué dimensiones de división se admiten para esta definición de métricas en la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="4466e-120">The strings indicate which break down dimensions are supported for this metric definition by the underlying instrumentation.</span></span> <span data-ttu-id="4466e-121">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="4466e-122">**Calculado**</span><span class="sxs-lookup"><span data-stu-id="4466e-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-125">Describe las características de la métrica con el fin de realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="4466e-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="4466e-126">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="4466e-127">Puede ser **null** o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4466e-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="4466e-128">Value</span><span class="sxs-lookup"><span data-stu-id="4466e-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4466e-129">Significado</span><span class="sxs-lookup"><span data-stu-id="4466e-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="4466e-130"><dt>**No calculado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="4466e-131">No se puede calcular el valor.</span><span class="sxs-lookup"><span data-stu-id="4466e-131">The value cannot be calculated.</span></span> <span data-ttu-id="4466e-132">Por ejemplo, una cadena.</span><span class="sxs-lookup"><span data-stu-id="4466e-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="4466e-133"><dt>**Sumable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="4466e-134">El valor se puede sumar en muchas instancias.</span><span class="sxs-lookup"><span data-stu-id="4466e-134">The value can be summed over many instances.</span></span> <span data-ttu-id="4466e-135">Por ejemplo, si cada trabajo de copia de seguridad es una unidad de trabajo y cada trabajo realiza una copia de seguridad de 27.000 archivos como promedio, los trabajos de copia de seguridad de 100 procesan los archivos 2,7 millones.</span><span class="sxs-lookup"><span data-stu-id="4466e-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="4466e-136"><dt> **No Resumable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="4466e-137">Este valor no se puede sumar en muchas instancias.</span><span class="sxs-lookup"><span data-stu-id="4466e-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="4466e-138">Un ejemplo sería una métrica que mide la longitud de la cola cuando un trabajo llega a un servidor.</span><span class="sxs-lookup"><span data-stu-id="4466e-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="4466e-139">Si cada trabajo es una unidad de trabajo y el promedio de longitud de cola cuando llega cada trabajo es 33, no tiene sentido decir que la longitud de la cola para los trabajos de 100 es 3300.</span><span class="sxs-lookup"><span data-stu-id="4466e-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="4466e-140">Tiene sentido decir que la media es 33.</span><span class="sxs-lookup"><span data-stu-id="4466e-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4466e-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4466e-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-144">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4466e-144">A short description of the object.</span></span> <span data-ttu-id="4466e-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4466e-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4466e-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="4466e-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-149">Indica cómo cambia el valor de la métrica, en forma de combinaciones típicas de atributos granulares más finos, como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.</span><span class="sxs-lookup"><span data-stu-id="4466e-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="4466e-150">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="4466e-151">Value</span><span class="sxs-lookup"><span data-stu-id="4466e-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="4466e-152">Significado</span><span class="sxs-lookup"><span data-stu-id="4466e-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4466e-153"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4466e-154">El diseñador de métricas no calificó el **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="4466e-154">The metric designer did not qualify the **ChangeType**.</span></span><br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="4466e-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="4466e-156">Si la propiedad **IsContinuous** es "false", **ChangeType** no tiene sentido y debe establecerse en "N/A".</span><span class="sxs-lookup"><span data-stu-id="4466e-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="4466e-157"><dt>**Contador**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="4466e-158">La métrica es una métrica de contador.</span><span class="sxs-lookup"><span data-stu-id="4466e-158">The metric is a counter metric.</span></span> <span data-ttu-id="4466e-159">Tienen valores enteros no negativos que aumentan hasta alcanzar el número máximo representable y, a continuación, se ajustan y comienzan a aumentar desde 0.</span><span class="sxs-lookup"><span data-stu-id="4466e-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="4466e-160"><dt>**Medidor**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="4466e-161">La métrica es una métrica del medidor.</span><span class="sxs-lookup"><span data-stu-id="4466e-161">The metric is a gauge metric.</span></span> <span data-ttu-id="4466e-162">Tienen valores enteros o flotantes que pueden aumentar y disminuir arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="4466e-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="4466e-163"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="4466e-164">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="4466e-165">Los proveedores pueden extender la propiedad **ChangeType** en el intervalo reservado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4466e-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="4466e-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="4466e-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-169">El tipo de datos de la métrica.</span><span class="sxs-lookup"><span data-stu-id="4466e-169">The data type of the metric.</span></span> <span data-ttu-id="4466e-170">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="4466e-171"><span id="boolean"></span><span id="BOOLEAN"></span>**booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="4466e-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="4466e-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="4466e-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="4466e-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="4466e-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="4466e-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="4466e-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="4466e-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="4466e-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-180"><span id="string"></span><span id="STRING"></span>**cadena** (10)</span><span class="sxs-lookup"><span data-stu-id="4466e-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="4466e-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="4466e-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="4466e-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="4466e-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4466e-185">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4466e-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-188">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4466e-188">A description of the object.</span></span> <span data-ttu-id="4466e-189">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4466e-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4466e-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4466e-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-193">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4466e-193">A display name for the object.</span></span> <span data-ttu-id="4466e-194">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4466e-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4466e-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="4466e-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-198">Indica cómo se recopilan los valores de métricas mediante la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="4466e-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="4466e-199">Esto permite a la aplicación cliente elegir la métrica adecuada para el propósito.</span><span class="sxs-lookup"><span data-stu-id="4466e-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="4466e-200">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="4466e-201">Puede ser **null** o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4466e-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="4466e-202">Value</span><span class="sxs-lookup"><span data-stu-id="4466e-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="4466e-203">Significado</span><span class="sxs-lookup"><span data-stu-id="4466e-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4466e-204"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4466e-205">No se conoce el tipo de recopilación.</span><span class="sxs-lookup"><span data-stu-id="4466e-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="4466e-206"><dt>**Onchange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="4466e-207">Los valores de métricas se actualizan inmediatamente cuando cambian los valores dentro del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="4466e-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="4466e-208"><dt>**Periódico**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="4466e-209">Los valores de métricas se actualizan periódicamente.</span><span class="sxs-lookup"><span data-stu-id="4466e-209">The metric values get updated periodically.</span></span> <span data-ttu-id="4466e-210">Por ejemplo, en una aplicación cliente, un valor de métrica que se aplica a la hora actual aparecerá como constante durante cada intervalo de recopilación y, a continuación, saltará al nuevo valor al final de cada intervalo de recopilación.</span><span class="sxs-lookup"><span data-stu-id="4466e-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="4466e-211"><dt>**Solicitud**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="4466e-212">El valor de métrica se determina cada vez que una aplicación cliente lo lee.</span><span class="sxs-lookup"><span data-stu-id="4466e-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="4466e-213"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="4466e-214">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="4466e-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="4466e-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4466e-218">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4466e-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4466e-219">Cadena que identifica de forma única la definición de la métrica.</span><span class="sxs-lookup"><span data-stu-id="4466e-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="4466e-220">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="4466e-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4466e-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4466e-224">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4466e-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4466e-225">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4466e-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4466e-226">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4466e-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4466e-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="4466e-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-228">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4466e-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-230">Indica si el valor de la métrica es continuo o escalar.</span><span class="sxs-lookup"><span data-stu-id="4466e-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="4466e-231">Las métricas de rendimiento son un ejemplo de una métrica continua.</span><span class="sxs-lookup"><span data-stu-id="4466e-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="4466e-232">Entre los ejemplos de métricas escalares se incluyen códigos de error o Estados operativos.</span><span class="sxs-lookup"><span data-stu-id="4466e-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="4466e-233">Las métricas continuas se pueden comparar utilizando la relación "mayor que".</span><span class="sxs-lookup"><span data-stu-id="4466e-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="4466e-234">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="4466e-235">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4466e-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-238">El nombre de la métrica.</span><span class="sxs-lookup"><span data-stu-id="4466e-238">The name of the metric.</span></span> <span data-ttu-id="4466e-239">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="4466e-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="4466e-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-243">Identifica las unidades específicas de un valor.</span><span class="sxs-lookup"><span data-stu-id="4466e-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="4466e-244">El valor de esta propiedad será un valor válido del calificador de unidades de programación, tal y como se define en el Apéndice C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o posterior.</span><span class="sxs-lookup"><span data-stu-id="4466e-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="4466e-245">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="4466e-246">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="4466e-246">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-248">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4466e-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4466e-249">Identifica el cálculo básico realizado en una métrica subyacente para llegar al valor de esta métrica derivada.</span><span class="sxs-lookup"><span data-stu-id="4466e-249">Identifies the basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="4466e-250">Esta propiedad se hereda de **CIM \_ AggregationMetricDefinition** y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4466e-250">This property is inherited from **CIM\_AggregationMetricDefinition** and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4466e-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="4466e-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="4466e-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Promedio** (4)</span><span class="sxs-lookup"><span data-stu-id="4466e-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)</span><span class="sxs-lookup"><span data-stu-id="4466e-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4466e-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo** (6)</span><span class="sxs-lookup"><span data-stu-id="4466e-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4466e-256">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="4466e-256">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4466e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-259">Indica el ámbito de tiempo al que se aplica el valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="4466e-259">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="4466e-260">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-260">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="4466e-261">Value</span><span class="sxs-lookup"><span data-stu-id="4466e-261">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="4466e-262">Significado</span><span class="sxs-lookup"><span data-stu-id="4466e-262">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4466e-263"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-263"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4466e-264">El diseñador de métricas no calificó el ámbito de tiempo o es desconocido para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="4466e-264">The time scope was not qualified by the metric designer, or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="4466e-265"><dt>**Punto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-265"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="4466e-266">La métrica se aplica a un momento dado.</span><span class="sxs-lookup"><span data-stu-id="4466e-266">The metric applies to a point in time.</span></span> <span data-ttu-id="4466e-267">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el momento dado y la propiedad **Duration** siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="4466e-267">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="4466e-268"><dt>**Intervalo**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-268"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="4466e-269">La métrica se aplica a un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4466e-269">The metric applies to a time interval.</span></span> <span data-ttu-id="4466e-270">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el final del intervalo de tiempo y la propiedad **Duration** especifica su duración.</span><span class="sxs-lookup"><span data-stu-id="4466e-270">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="4466e-271"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-271"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="4466e-272">La métrica se aplica a un intervalo de tiempo que comenzó en el inicio del recurso medido (es decir, el ManagedElement asociado a MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="4466e-272">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="4466e-273">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el final del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4466e-273">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="4466e-274">Si la propiedad **Duration** es 0, indica que se desconoce la hora de inicio del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="4466e-274">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="4466e-275">De lo contrario, **Duration** especifica la duración entre el inicio del recurso y la **marca** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4466e-275">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="4466e-276"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-276"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="4466e-277">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-277"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="4466e-278">**Unidades**</span><span class="sxs-lookup"><span data-stu-id="4466e-278">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4466e-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4466e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4466e-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4466e-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4466e-281">Identifica las unidades de un valor, por ejemplo, "megabytes".</span><span class="sxs-lookup"><span data-stu-id="4466e-281">Identifies the units of a value, for example, "megabytes".</span></span> <span data-ttu-id="4466e-282">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="4466e-282">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4466e-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4466e-283">Requirements</span></span>



| <span data-ttu-id="4466e-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="4466e-284">Requirement</span></span> | <span data-ttu-id="4466e-285">Value</span><span class="sxs-lookup"><span data-stu-id="4466e-285">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4466e-286">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4466e-286">Minimum supported client</span></span><br/> | <span data-ttu-id="4466e-287">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4466e-287">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4466e-288">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4466e-288">Minimum supported server</span></span><br/> | <span data-ttu-id="4466e-289">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4466e-289">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4466e-290">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4466e-290">Namespace</span></span><br/>                | <span data-ttu-id="4466e-291">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4466e-291">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4466e-292">MOF</span><span class="sxs-lookup"><span data-stu-id="4466e-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4466e-293"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-293"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4466e-294">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4466e-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4466e-295"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-295"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

