---
description: Representa los aspectos de la definición de una métrica.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688724"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="8c02b-103">MSVM \_ BaseMetricDefinition (clase)</span><span class="sxs-lookup"><span data-stu-id="8c02b-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="8c02b-104">Representa los aspectos de la definición de una métrica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="8c02b-105">La clase **MSVM \_ BaseMetricDefinition** debe estar asociada a la [**\_ ManagedElements CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) a la que se aplica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="8c02b-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8c02b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c02b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c02b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
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
};
```

## <a name="members"></a><span data-ttu-id="8c02b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c02b-108">Members</span></span>

<span data-ttu-id="8c02b-109">La clase **MSVM \_ BaseMetricDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c02b-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="8c02b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c02b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c02b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c02b-111">Properties</span></span>

<span data-ttu-id="8c02b-112">La clase **MSVM \_ BaseMetricDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c02b-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c02b-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="8c02b-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8c02b-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-116">Define una o más cadenas que se pueden usar para refinar (dividir) las consultas con los valores de métrica a lo largo de una dimensión determinada.</span><span class="sxs-lookup"><span data-stu-id="8c02b-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="8c02b-117">Un ejemplo es un nombre de transacción, lo que permite el desglose del valor total de todas las transacciones en un conjunto de valores, uno para cada nombre de transacción.</span><span class="sxs-lookup"><span data-stu-id="8c02b-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="8c02b-118">Otros ejemplos podrían ser sistema de aplicaciones o nombre de grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="8c02b-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="8c02b-119">Las cadenas tienen un formato libre y deben ser significativas para los usuarios finales de los datos de métricas.</span><span class="sxs-lookup"><span data-stu-id="8c02b-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="8c02b-120">Las cadenas indican qué dimensiones de división se admiten para esta definición de métricas, mediante la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="8c02b-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="8c02b-121">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-122">**Calculado**</span><span class="sxs-lookup"><span data-stu-id="8c02b-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c02b-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-125">Describe las características de la métrica con el fin de realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="8c02b-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="8c02b-126">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="8c02b-127">Puede ser **null** o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c02b-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="8c02b-128">Value</span><span class="sxs-lookup"><span data-stu-id="8c02b-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="8c02b-129">Significado</span><span class="sxs-lookup"><span data-stu-id="8c02b-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="8c02b-130"><dt>**No calculado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8c02b-131">No se puede calcular el valor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-131">The value cannot be calculated.</span></span> <span data-ttu-id="8c02b-132">Por ejemplo, una cadena.</span><span class="sxs-lookup"><span data-stu-id="8c02b-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="8c02b-133"><dt>**Sumable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="8c02b-134">El valor se puede sumar en muchas instancias.</span><span class="sxs-lookup"><span data-stu-id="8c02b-134">The value can be summed over many instances.</span></span> <span data-ttu-id="8c02b-135">Por ejemplo, si cada trabajo de copia de seguridad es una unidad de trabajo y cada trabajo realiza una copia de seguridad de 27.000 archivos como promedio, los trabajos de copia de seguridad de 100 procesan los archivos 2,7 millones.</span><span class="sxs-lookup"><span data-stu-id="8c02b-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="8c02b-136"><dt> **No Resumable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="8c02b-137">Este valor no se puede sumar en muchas instancias.</span><span class="sxs-lookup"><span data-stu-id="8c02b-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="8c02b-138">Un ejemplo sería una métrica que mide la longitud de la cola cuando un trabajo llega a un servidor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="8c02b-139">Si cada trabajo es una unidad de trabajo y el promedio de longitud de cola cuando llega cada trabajo es 33, no tiene sentido decir que la longitud de la cola para los trabajos de 100 es 3300.</span><span class="sxs-lookup"><span data-stu-id="8c02b-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="8c02b-140">Tiene sentido decir que la media es 33.</span><span class="sxs-lookup"><span data-stu-id="8c02b-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c02b-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8c02b-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-144">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c02b-144">A short description of the object.</span></span> <span data-ttu-id="8c02b-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8c02b-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="8c02b-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c02b-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-149">Indica cómo cambia el valor de la métrica, en forma de combinaciones típicas de atributos granulares más finos, como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.</span><span class="sxs-lookup"><span data-stu-id="8c02b-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="8c02b-150">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="8c02b-151">Value</span><span class="sxs-lookup"><span data-stu-id="8c02b-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8c02b-152">Significado</span><span class="sxs-lookup"><span data-stu-id="8c02b-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8c02b-153"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="8c02b-154">El diseñador de métricas no calificó el **ChangeType.**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="8c02b-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="8c02b-156">Si la propiedad **IsContinuous** es "false", **ChangeType** no tiene sentido y debe establecerse en "N/A".</span><span class="sxs-lookup"><span data-stu-id="8c02b-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="8c02b-157"><dt>**Contador**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="8c02b-158">La métrica es una métrica de contador.</span><span class="sxs-lookup"><span data-stu-id="8c02b-158">The metric is a counter metric.</span></span> <span data-ttu-id="8c02b-159">Tienen valores enteros no negativos que aumentan hasta alcanzar el número máximo representable y, a continuación, se ajustan y comienzan a aumentar desde 0.</span><span class="sxs-lookup"><span data-stu-id="8c02b-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="8c02b-160"><dt>**Medidor**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="8c02b-161">La métrica es una métrica del medidor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-161">The metric is a gauge metric.</span></span> <span data-ttu-id="8c02b-162">Tienen valores enteros o flotantes que pueden aumentar y disminuir arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="8c02b-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8c02b-163"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="8c02b-164">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="8c02b-165">Los proveedores pueden extender la propiedad **ChangeType** en el intervalo reservado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="8c02b-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="8c02b-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c02b-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-169">El tipo de datos de la métrica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-169">The data type of the metric.</span></span> <span data-ttu-id="8c02b-170">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="8c02b-171"><span id="boolean"></span><span id="BOOLEAN"></span>**booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="8c02b-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="8c02b-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="8c02b-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="8c02b-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="8c02b-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="8c02b-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="8c02b-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="8c02b-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="8c02b-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-180"><span id="string"></span><span id="STRING"></span>**cadena** (10)</span><span class="sxs-lookup"><span data-stu-id="8c02b-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="8c02b-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="8c02b-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="8c02b-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="8c02b-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c02b-185">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c02b-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-188">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c02b-188">A description of the object.</span></span> <span data-ttu-id="8c02b-189">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8c02b-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8c02b-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-193">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c02b-193">A display name for the object.</span></span> <span data-ttu-id="8c02b-194">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8c02b-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="8c02b-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c02b-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-198">Indica cómo se recopilan los valores de métricas mediante la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="8c02b-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="8c02b-199">Esto permite a la aplicación cliente elegir la métrica adecuada para el propósito.</span><span class="sxs-lookup"><span data-stu-id="8c02b-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="8c02b-200">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="8c02b-201">Puede ser **null** o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c02b-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="8c02b-202">Value</span><span class="sxs-lookup"><span data-stu-id="8c02b-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8c02b-203">Significado</span><span class="sxs-lookup"><span data-stu-id="8c02b-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8c02b-204"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="8c02b-205">No se conoce el tipo de recopilación.</span><span class="sxs-lookup"><span data-stu-id="8c02b-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="8c02b-206"><dt>**Onchange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="8c02b-207">Los valores de métricas se actualizan inmediatamente cuando cambian los valores dentro del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="8c02b-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="8c02b-208"><dt>**Periódico**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8c02b-209">Los valores de métricas se actualizan periódicamente.</span><span class="sxs-lookup"><span data-stu-id="8c02b-209">The metric values get updated periodically.</span></span> <span data-ttu-id="8c02b-210">Por ejemplo, en una aplicación cliente, un valor de métrica que se aplica a la hora actual aparecerá como constante durante cada intervalo de recopilación y, a continuación, saltará al nuevo valor al final de cada intervalo de recopilación.</span><span class="sxs-lookup"><span data-stu-id="8c02b-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="8c02b-211"><dt>**Solicitud**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="8c02b-212">El valor de métrica se determina cada vez que una aplicación cliente lo lee.</span><span class="sxs-lookup"><span data-stu-id="8c02b-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8c02b-213"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="8c02b-214">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8c02b-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="8c02b-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-218">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8c02b-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-219">Cadena que identifica de forma única la definición de la métrica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="8c02b-220">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c02b-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-224">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8c02b-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-225">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8c02b-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8c02b-226">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8c02b-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="8c02b-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-228">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8c02b-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-230">Indica si el valor de la métrica es continuo o escalar.</span><span class="sxs-lookup"><span data-stu-id="8c02b-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="8c02b-231">Las métricas de rendimiento son un ejemplo de una métrica continua.</span><span class="sxs-lookup"><span data-stu-id="8c02b-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="8c02b-232">Entre los ejemplos de métricas escalares se incluyen códigos de error o Estados operativos.</span><span class="sxs-lookup"><span data-stu-id="8c02b-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="8c02b-233">Las métricas continuas se pueden comparar utilizando la relación "mayor que".</span><span class="sxs-lookup"><span data-stu-id="8c02b-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="8c02b-234">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-235">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8c02b-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-238">El nombre de la métrica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-238">The name of the metric.</span></span> <span data-ttu-id="8c02b-239">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="8c02b-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-243">Identifica las unidades específicas de un valor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="8c02b-244">El valor de esta propiedad será un valor válido del calificador de unidades de programación, tal y como se define en el Apéndice C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o posterior.</span><span class="sxs-lookup"><span data-stu-id="8c02b-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="8c02b-245">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="8c02b-246">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="8c02b-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c02b-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-249">Indica el ámbito de tiempo al que se aplica el valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="8c02b-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="8c02b-250">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="8c02b-251">Value</span><span class="sxs-lookup"><span data-stu-id="8c02b-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8c02b-252">Significado</span><span class="sxs-lookup"><span data-stu-id="8c02b-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8c02b-253"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="8c02b-254">El diseñador de métricas no calificó el ámbito de tiempo o es desconocido para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8c02b-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="8c02b-255"><dt>**Punto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="8c02b-256">La métrica se aplica a un momento dado.</span><span class="sxs-lookup"><span data-stu-id="8c02b-256">The metric applies to a point in time.</span></span> <span data-ttu-id="8c02b-257">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el momento dado y la propiedad **Duration** siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="8c02b-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="8c02b-258"><dt>**Intervalo**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8c02b-259">La métrica se aplica a un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8c02b-259">The metric applies to a time interval.</span></span> <span data-ttu-id="8c02b-260">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el final del intervalo de tiempo y la propiedad **Duration** especifica su duración.</span><span class="sxs-lookup"><span data-stu-id="8c02b-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="8c02b-261"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="8c02b-262">La métrica se aplica a un intervalo de tiempo que comenzó en el inicio del recurso medido (es decir, el ManagedElement asociado a MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="8c02b-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="8c02b-263">En las instancias [**de \_ BaseMetricValue de MSVM**](msvm-basemetricvalue.md) correspondientes, la propiedad **timestamp** especifica el final del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8c02b-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="8c02b-264">Si la propiedad **Duration** es 0, indica que se desconoce la hora de inicio del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="8c02b-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="8c02b-265">De lo contrario, **Duration** especifica la duración entre el inicio del recurso y la **marca** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8c02b-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8c02b-266"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="8c02b-267">El <dt> **proveedor**</dt> es el <dt>32768 reservado... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="8c02b-268">**Unidades**</span><span class="sxs-lookup"><span data-stu-id="8c02b-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c02b-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c02b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c02b-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c02b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c02b-271">Identifica las unidades específicas de un valor, por ejemplo, "megabytes".</span><span class="sxs-lookup"><span data-stu-id="8c02b-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="8c02b-272">Esta propiedad se hereda de **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="8c02b-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c02b-273">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c02b-273">Requirements</span></span>



| <span data-ttu-id="8c02b-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c02b-274">Requirement</span></span> | <span data-ttu-id="8c02b-275">Value</span><span class="sxs-lookup"><span data-stu-id="8c02b-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c02b-276">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c02b-276">Minimum supported client</span></span><br/> | <span data-ttu-id="8c02b-277">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c02b-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c02b-278">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c02b-278">Minimum supported server</span></span><br/> | <span data-ttu-id="8c02b-279">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c02b-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c02b-280">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c02b-280">Namespace</span></span><br/>                | <span data-ttu-id="8c02b-281">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8c02b-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8c02b-282">MOF</span><span class="sxs-lookup"><span data-stu-id="8c02b-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c02b-283"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c02b-284">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c02b-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c02b-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c02b-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

