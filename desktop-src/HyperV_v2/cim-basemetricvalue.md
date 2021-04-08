---
description: Representa el valor de instancia de una métrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002571"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="d461f-103">\_Clase BaseMetricValue de CIM</span><span class="sxs-lookup"><span data-stu-id="d461f-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="d461f-104">Representa el valor de instancia de una métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="d461f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d461f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="d461f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d461f-106">Members</span></span>

<span data-ttu-id="d461f-107">La clase **CIM \_ BaseMetricValue** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d461f-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="d461f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d461f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d461f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d461f-109">Properties</span></span>

<span data-ttu-id="d461f-110">La clase **CIM \_ BaseMetricValue** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d461f-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d461f-111">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="d461f-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d461f-114">Dimensión para la que este conjunto de valores de métrica se divide en función de la propiedad **BreakdownDimensions** del [**objeto \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="d461f-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-115">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="d461f-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d461f-118">Valor de la propiedad **BreakdownDimension** definida para este valor de instancia.</span><span class="sxs-lookup"><span data-stu-id="d461f-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="d461f-119">Por ejemplo, si **BreakdownDimension** contiene "TransactionName", esta propiedad podría nombrar la transacción real a la que se aplica este valor de métrica en particular.</span><span class="sxs-lookup"><span data-stu-id="d461f-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-120">**Duration**</span><span class="sxs-lookup"><span data-stu-id="d461f-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-121">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d461f-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d461f-123">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**\_ BaseMetricValue CIM**.**Marca** de tiempo ")</span><span class="sxs-lookup"><span data-stu-id="d461f-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="d461f-124">La duración de la validez de este valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="d461f-125">Esta propiedad no debe existir para las marcas de tiempo que solo se aplican a un punto en el tiempo, pero debe definirse para los valores que se consideran válidos durante un período de tiempo determinado (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="d461f-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="d461f-126">muestreo).</span><span class="sxs-lookup"><span data-stu-id="d461f-126">sampling).</span></span> <span data-ttu-id="d461f-127">Si la propiedad duration existe y no es null, el valor de **marca** de **tiempo** debe ser el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="d461f-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d461f-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d461f-131">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="d461f-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="d461f-132">Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="d461f-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d461f-133">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="d461f-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="d461f-134">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="d461f-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="d461f-135">Este patrón es similar a la estructura de los nombres de clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="d461f-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="d461f-136">Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="d461f-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="d461f-137">Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').</span><span class="sxs-lookup"><span data-stu-id="d461f-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="d461f-138">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="d461f-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="d461f-139">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d461f-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="d461f-140">En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="d461f-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="d461f-141">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="d461f-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d461f-144">Nombre descriptivo para el elemento que mide la métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="d461f-145">Esta propiedad es necesaria si la definición de la métrica no está asociada a un objeto [**\_ ManagedElement de CIM**](cim-managedelement.md) y se puede usar en otros casos para proporcionar información complementaria.</span><span class="sxs-lookup"><span data-stu-id="d461f-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="d461f-146">Esto permite capturar las métricas independientemente de cualquier objeto **\_ ManagedElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="d461f-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="d461f-147">Si hay varios objetos [**de \_ ManagedElement de CIM**](cim-managedelement.md) asociados al valor de métricas, puede elegir uno de los elementos administrados para crear la información complementaria de la métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="d461f-148">La propiedad no está diseñada para utilizarse como clave externa para consultar el elemento medido.</span><span class="sxs-lookup"><span data-stu-id="d461f-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="d461f-149">En su lugar, se debe usar la asociación con el **\_ ManagedElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="d461f-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="d461f-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d461f-153">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")</span><span class="sxs-lookup"><span data-stu-id="d461f-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="d461f-154">La clave de la instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que está asociada a este valor de instancia.</span><span class="sxs-lookup"><span data-stu-id="d461f-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-155">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="d461f-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d461f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d461f-158">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d461f-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d461f-159">Representación de cadena del valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-159">A string representation of the metric value.</span></span> <span data-ttu-id="d461f-160">El tipo de datos original del valor de métrica se especifica en el objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="d461f-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-161">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="d461f-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d461f-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d461f-164">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**\_ BaseMetricValue CIM**.**Duration**")</span><span class="sxs-lookup"><span data-stu-id="d461f-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="d461f-165">La hora a la que se calcula el valor de una instancia de métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="d461f-166">Esto es diferente del momento en que se crea la instancia.</span><span class="sxs-lookup"><span data-stu-id="d461f-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="d461f-167">Si la propiedad **volatile** es true, este valor cambia cada vez que se toma una nueva instantánea de medida.</span><span class="sxs-lookup"><span data-stu-id="d461f-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="d461f-168">Una aplicación de administración puede establecer una serie temporal de datos de métricas mediante la recuperación de las instancias de **CIM \_ BaseMetricValue** y ordenarlas según su valor de **marca** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d461f-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="d461f-169">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="d461f-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d461f-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d461f-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d461f-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d461f-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d461f-172">True si el valor de **marca** de tiempo cambia cada vez que cambia el valor de la instancia de métrica.</span><span class="sxs-lookup"><span data-stu-id="d461f-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="d461f-173">False si este objeto debe permanecer sin cambios y se ha creado un nuevo objeto para el nuevo valor de **marca** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d461f-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d461f-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d461f-174">Requirements</span></span>



| <span data-ttu-id="d461f-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d461f-175">Requirement</span></span> | <span data-ttu-id="d461f-176">Value</span><span class="sxs-lookup"><span data-stu-id="d461f-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d461f-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d461f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d461f-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d461f-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d461f-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d461f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d461f-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d461f-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d461f-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d461f-181">Namespace</span></span><br/>                | <span data-ttu-id="d461f-182">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d461f-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d461f-183">MOF</span><span class="sxs-lookup"><span data-stu-id="d461f-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d461f-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d461f-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d461f-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d461f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d461f-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d461f-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d461f-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="d461f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d461f-188">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d461f-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

