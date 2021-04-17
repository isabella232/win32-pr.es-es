---
description: Representa una definición de métrica que contiene los metadatos para un \_ objeto MetricInstance de CIM.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669949"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="f292a-103">\_Clase BaseMetricDefinition de CIM</span><span class="sxs-lookup"><span data-stu-id="f292a-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="f292a-104">Representa una definición de métrica que contiene los metadatos para un objeto **\_ MetricInstance de CIM** .</span><span class="sxs-lookup"><span data-stu-id="f292a-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f292a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f292a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="f292a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f292a-106">Members</span></span>

<span data-ttu-id="f292a-107">La clase **CIM \_ BaseMetricDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f292a-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="f292a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f292a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f292a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f292a-109">Properties</span></span>

<span data-ttu-id="f292a-110">La clase **CIM \_ BaseMetricDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f292a-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f292a-111">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="f292a-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-112">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f292a-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f292a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-114">Una matriz que contiene cadenas de formato libre que se pueden usar para desglosar las consultas de objetos [**\_ BaseMetricValue de CIM**](cim-basemetricvalue.md) a lo largo de una dimensión determinada.</span><span class="sxs-lookup"><span data-stu-id="f292a-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="f292a-115">Las cadenas deben ser significativas para los usuarios finales de los datos de métricas.</span><span class="sxs-lookup"><span data-stu-id="f292a-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="f292a-116">Además, las cadenas deben indicar qué dimensiones de división se admiten para la definición de métricas, mediante la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="f292a-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="f292a-117">Un ejemplo es un nombre de transacción que permite el desglose del valor total de todas las transacciones en un conjunto de valores, uno para cada nombre de transacción.</span><span class="sxs-lookup"><span data-stu-id="f292a-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="f292a-118">Otros ejemplos son un sistema de aplicaciones o un nombre de grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="f292a-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="f292a-119">**Calculado**</span><span class="sxs-lookup"><span data-stu-id="f292a-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-120">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f292a-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-122">Características de la métrica que se usan para realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="f292a-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="f292a-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**No calculado** (1)</span><span class="sxs-lookup"><span data-stu-id="f292a-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-124">Una cadena.</span><span class="sxs-lookup"><span data-stu-id="f292a-124">A string.</span></span> <span data-ttu-id="f292a-125">La aritmética no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="f292a-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="f292a-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sumable** (2)</span><span class="sxs-lookup"><span data-stu-id="f292a-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-127">Es razonable sumar este valor en muchas instancias de, por ejemplo, UnitOfWork, como el número de archivos procesados en un trabajo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f292a-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="f292a-128">Por ejemplo, si cada trabajo de copia de seguridad es un UnitOfWork y cada trabajo realiza una copia de seguridad de 27.000 archivos como promedio, tiene sentido decir que los trabajos de copia de seguridad de 100 procesaron 2,7 millones archivos.</span><span class="sxs-lookup"><span data-stu-id="f292a-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="f292a-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**No sumable** (3)</span><span class="sxs-lookup"><span data-stu-id="f292a-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-130">No tiene sentido sumar este valor en muchas instancias de UnitOfWork.</span><span class="sxs-lookup"><span data-stu-id="f292a-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="f292a-131">Un ejemplo sería una métrica que mide la longitud de la cola cuando un trabajo llega a un servidor.</span><span class="sxs-lookup"><span data-stu-id="f292a-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="f292a-132">Si cada trabajo es un UnitOfWork y el promedio de longitud de cola cuando llega cada trabajo es 33, no tiene sentido decir que la longitud de la cola para los trabajos de 100 es 3300.</span><span class="sxs-lookup"><span data-stu-id="f292a-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="f292a-133">Tiene sentido decir que la media es 33.</span><span class="sxs-lookup"><span data-stu-id="f292a-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f292a-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="f292a-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f292a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f292a-137">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")</span><span class="sxs-lookup"><span data-stu-id="f292a-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="f292a-138">Indica cómo cambia el valor de métrica mediante atributos comunes como el cambio de dirección, los valores mínimo y máximo y la semántica de ajuste.</span><span class="sxs-lookup"><span data-stu-id="f292a-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f292a-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f292a-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-140">El diseñador de métricas no calificó el ChangeType.</span><span class="sxs-lookup"><span data-stu-id="f292a-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="f292a-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span><span class="sxs-lookup"><span data-stu-id="f292a-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-142">Si la propiedad "IsContinuous" es "false", ChangeType no tiene sentido y debe establecerse en "N/A".</span><span class="sxs-lookup"><span data-stu-id="f292a-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="f292a-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contador** (3)</span><span class="sxs-lookup"><span data-stu-id="f292a-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-144">La métrica es una métrica de contador.</span><span class="sxs-lookup"><span data-stu-id="f292a-144">The metric is a counter metric.</span></span> <span data-ttu-id="f292a-145">Tienen valores enteros no negativos que aumentan de forma monotónica hasta alcanzar el número máximo representable y, a continuación, se ajustan y comienzan a aumentar desde 0.</span><span class="sxs-lookup"><span data-stu-id="f292a-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="f292a-146">Estos contadores, también conocidos como contadores de sustitución incremental, se pueden usar para que la instancia cuente el número de errores de red o el número de transacciones procesadas.</span><span class="sxs-lookup"><span data-stu-id="f292a-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="f292a-147">La única manera de que una aplicación cliente realice un seguimiento de las contornos consiste en recuperar el valor del contador en intervalos de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="f292a-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="f292a-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Medidor** (4)</span><span class="sxs-lookup"><span data-stu-id="f292a-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-149">La métrica es una métrica del medidor.</span><span class="sxs-lookup"><span data-stu-id="f292a-149">The metric is a gauge metric.</span></span> <span data-ttu-id="f292a-150">Tienen valores enteros o flotantes que pueden aumentar y disminuir arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="f292a-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="f292a-151">Un medidor no debe ajustarse cuando se alcanza el número mínimo o máximo que se represente, en su lugar, el valor "se ciñe" en ese número.</span><span class="sxs-lookup"><span data-stu-id="f292a-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="f292a-152">Los valores mínimos o máximos dentro del intervalo de valores representables en los que el valor de métrica se "palo" se pueden definir o no.</span><span class="sxs-lookup"><span data-stu-id="f292a-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f292a-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f292a-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f292a-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f292a-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f292a-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="f292a-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-156">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f292a-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-158">El tipo de datos de la métrica.</span><span class="sxs-lookup"><span data-stu-id="f292a-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="f292a-159">**booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="f292a-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="f292a-160">**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="f292a-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="f292a-161">**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="f292a-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="f292a-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="f292a-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="f292a-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="f292a-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="f292a-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="f292a-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="f292a-165">**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="f292a-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="f292a-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="f292a-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="f292a-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="f292a-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="f292a-168">**cadena** (10)</span><span class="sxs-lookup"><span data-stu-id="f292a-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="f292a-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="f292a-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="f292a-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="f292a-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="f292a-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="f292a-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="f292a-172">**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="f292a-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f292a-173">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="f292a-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-174">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f292a-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-176">Indica cómo se recopilan los valores de métricas mediante la instrumentación subyacente.</span><span class="sxs-lookup"><span data-stu-id="f292a-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f292a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f292a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-178">Indica que no se conoce el GatheringType.</span><span class="sxs-lookup"><span data-stu-id="f292a-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="f292a-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**Onchange** (2)</span><span class="sxs-lookup"><span data-stu-id="f292a-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-180">Indica que los valores de métrica CIM se actualizan inmediatamente cuando cambian los valores dentro del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="f292a-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="f292a-181">Los valores de las métricas onchange reflejan realmente la situación actual del recurso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f292a-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="f292a-182">Un ejemplo es el número de usuarios que han iniciado sesión y que se actualizan inmediatamente a medida que los usuarios inician y cierran sesión.</span><span class="sxs-lookup"><span data-stu-id="f292a-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="f292a-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periódico** (3)</span><span class="sxs-lookup"><span data-stu-id="f292a-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-184">": Indica que los valores de métrica CIM se actualizan periódicamente.</span><span class="sxs-lookup"><span data-stu-id="f292a-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="f292a-185">Por ejemplo, en una aplicación cliente, un valor de métrica que se aplica a la hora actual aparecerá como constante durante cada intervalo de recopilación y, a continuación, saltará al nuevo valor al final de cada intervalo de recopilación.</span><span class="sxs-lookup"><span data-stu-id="f292a-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="f292a-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**Request** (4)</span><span class="sxs-lookup"><span data-stu-id="f292a-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-187">Indica que el valor de métrica CIM se determina cada vez que una aplicación cliente lo lee.</span><span class="sxs-lookup"><span data-stu-id="f292a-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="f292a-188">Los valores de las métricas de solicitud devuelven realmente la situación actual dentro del recurso si alguien la solicita.</span><span class="sxs-lookup"><span data-stu-id="f292a-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="f292a-189">Sin embargo, no cambian el valor "unobservado" y, por lo tanto, no se recomienda suscribir los cambios de valor de las métricas de solicitud.</span><span class="sxs-lookup"><span data-stu-id="f292a-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f292a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f292a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f292a-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f292a-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f292a-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="f292a-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f292a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f292a-195">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f292a-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f292a-196">IDENTIFICADOR único de la definición de métrica.</span><span class="sxs-lookup"><span data-stu-id="f292a-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="f292a-197">Se recomienda el UUID/GUID de Open Software Foundation (OSF).</span><span class="sxs-lookup"><span data-stu-id="f292a-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="f292a-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="f292a-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-199">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f292a-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-201">True si el valor de la métrica es continuo; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="f292a-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="f292a-202">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f292a-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f292a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-205">El nombre de la métrica.</span><span class="sxs-lookup"><span data-stu-id="f292a-205">The name of the metric.</span></span> <span data-ttu-id="f292a-206">Este nombre no tiene que ser único, pero debe ser descriptivo y puede contener espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="f292a-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="f292a-207">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="f292a-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f292a-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-210">Unidades específicas de un valor.</span><span class="sxs-lookup"><span data-stu-id="f292a-210">The specific units of a value.</span></span> <span data-ttu-id="f292a-211">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el Apéndice C. 1 de DSP0004 V 2.4 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f292a-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f292a-212">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="f292a-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f292a-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f292a-215">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**Marca** de tiempo ","**CIM \_ BaseMetricValue**.**Duration**")</span><span class="sxs-lookup"><span data-stu-id="f292a-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="f292a-216">El ámbito de tiempo que se aplica al diseñador de métricas.</span><span class="sxs-lookup"><span data-stu-id="f292a-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f292a-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f292a-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-218">Indica que el diseñador de métricas no calificó el ámbito de tiempo o es desconocido para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f292a-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="f292a-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punto** (2)</span><span class="sxs-lookup"><span data-stu-id="f292a-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-220">Indica que la métrica se aplica a un punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="f292a-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="f292a-221">En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el momento dado y Duration siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="f292a-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="f292a-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalo** (3)</span><span class="sxs-lookup"><span data-stu-id="f292a-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-223">Indica que la métrica se aplica a un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f292a-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="f292a-224">En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el final del intervalo de tiempo y Duration especifica su duración.</span><span class="sxs-lookup"><span data-stu-id="f292a-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="f292a-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span><span class="sxs-lookup"><span data-stu-id="f292a-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f292a-226">Indica que la métrica se aplica a un intervalo de tiempo que comenzó en el inicio del recurso medido (es decir, el ManagedElement asociado a MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="f292a-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="f292a-227">En las instancias de BaseMetricValue correspondientes, TimeStamp especifica el final del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f292a-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="f292a-228">Si Duration es 0, indica que se desconoce la hora de inicio del recurso medido.</span><span class="sxs-lookup"><span data-stu-id="f292a-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="f292a-229">En caso contrario, Duration especifica la duración entre el inicio del recurso y la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f292a-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f292a-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f292a-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f292a-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f292a-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f292a-232">**Unidades**</span><span class="sxs-lookup"><span data-stu-id="f292a-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f292a-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f292a-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f292a-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f292a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f292a-235">Unidades de la métrica.</span><span class="sxs-lookup"><span data-stu-id="f292a-235">The units of the metric.</span></span> <span data-ttu-id="f292a-236">Algunos ejemplos son bytes, paquetes, trabajos, archivos, milisegundos y amperios.</span><span class="sxs-lookup"><span data-stu-id="f292a-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f292a-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f292a-237">Requirements</span></span>



| <span data-ttu-id="f292a-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="f292a-238">Requirement</span></span> | <span data-ttu-id="f292a-239">Value</span><span class="sxs-lookup"><span data-stu-id="f292a-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f292a-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f292a-240">Minimum supported client</span></span><br/> | <span data-ttu-id="f292a-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f292a-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f292a-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f292a-242">Minimum supported server</span></span><br/> | <span data-ttu-id="f292a-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f292a-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f292a-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f292a-244">Namespace</span></span><br/>                | <span data-ttu-id="f292a-245">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f292a-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f292a-246">MOF</span><span class="sxs-lookup"><span data-stu-id="f292a-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f292a-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f292a-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f292a-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f292a-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f292a-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f292a-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f292a-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="f292a-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f292a-251">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f292a-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

