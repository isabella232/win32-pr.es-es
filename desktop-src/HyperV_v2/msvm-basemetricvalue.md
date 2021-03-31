---
description: Representa un valor de métrica definido por una instancia de la \_ clase MSVM BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912593"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="83ade-103">MSVM \_ BaseMetricValue (clase)</span><span class="sxs-lookup"><span data-stu-id="83ade-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="83ade-104">Representa un valor de métrica definido por una instancia de la clase [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="83ade-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="83ade-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="83ade-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ade-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83ade-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a><span data-ttu-id="83ade-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="83ade-107">Members</span></span>

<span data-ttu-id="83ade-108">La clase **MSVM \_ BaseMetricValue** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83ade-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="83ade-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83ade-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83ade-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83ade-110">Properties</span></span>

<span data-ttu-id="83ade-111">La clase **MSVM \_ BaseMetricValue** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83ade-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83ade-112">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="83ade-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-115">Especifica una dimensión de desglose de la matriz **BreakdownDimensions** definida en la [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="83ade-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="83ade-116">Esta es la dimensión en la que se divide este conjunto de valores de métricas.</span><span class="sxs-lookup"><span data-stu-id="83ade-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="83ade-117">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-118">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="83ade-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-121">Define un valor de la propiedad **BreakdownDimension** definida para esta instancia de valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="83ade-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="83ade-122">Por ejemplo, si **BreakdownDimension** es "TransactionName", esta propiedad podría nombrar la transacción real a la que se aplica este valor de métrica en particular.</span><span class="sxs-lookup"><span data-stu-id="83ade-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="83ade-123">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="83ade-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-127">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="83ade-127">A short description of the object.</span></span> <span data-ttu-id="83ade-128">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83ade-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-132">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="83ade-132">A description of the object.</span></span> <span data-ttu-id="83ade-133">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-134">**Duration**</span><span class="sxs-lookup"><span data-stu-id="83ade-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83ade-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-137">Especifica la duración de la validez de este valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="83ade-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="83ade-138">Esta propiedad no debe existir para las marcas de tiempo que se aplican solo a un punto en el tiempo, pero debe especificarse para los valores que se consideran válidos para un determinado período de tiempo (por ejemplo, muestreo).</span><span class="sxs-lookup"><span data-stu-id="83ade-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="83ade-139">Si la propiedad **Duration** existe y no es **null**, la propiedad **timestamp** especifica el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="83ade-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="83ade-140">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="83ade-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-144">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="83ade-144">A display name for the object.</span></span> <span data-ttu-id="83ade-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="83ade-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ade-149">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="83ade-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="83ade-150">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="83ade-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="83ade-151">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-152">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="83ade-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-155">Un nombre descriptivo para el elemento al que pertenece el valor de métrica (el elemento medido).</span><span class="sxs-lookup"><span data-stu-id="83ade-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="83ade-156">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="83ade-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-160">La clave de la instancia de [**\_ BaseMetricDefinition de MSVM**](msvm-basemetricdefinition.md) para este valor.</span><span class="sxs-lookup"><span data-stu-id="83ade-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="83ade-161">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-162">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="83ade-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83ade-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-165">Valor de la métrica que se representa como una cadena.</span><span class="sxs-lookup"><span data-stu-id="83ade-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="83ade-166">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-167">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="83ade-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-168">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83ade-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-170">Especifica la hora a la que se capturó o calculó el valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="83ade-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="83ade-171">Tenga en cuenta que esto es diferente del momento en que se creó la instancia.</span><span class="sxs-lookup"><span data-stu-id="83ade-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="83ade-172">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ade-173">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="83ade-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ade-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="83ade-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83ade-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83ade-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ade-176">**True** si el valor para el siguiente punto en el tiempo usará la misma instancia de la clase y simplemente cambiará los valores de propiedad (como el **valor** o la **marca** de tiempo).</span><span class="sxs-lookup"><span data-stu-id="83ade-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="83ade-177">Si es **true**, la instancia se reutiliza.</span><span class="sxs-lookup"><span data-stu-id="83ade-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="83ade-178">Si **es false**, las instancias existentes permanecen sin cambios y se crea una nueva instancia para el nuevo punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="83ade-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="83ade-179">Esta propiedad se hereda de [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ade-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83ade-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83ade-180">Requirements</span></span>



| <span data-ttu-id="83ade-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="83ade-181">Requirement</span></span> | <span data-ttu-id="83ade-182">Value</span><span class="sxs-lookup"><span data-stu-id="83ade-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ade-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83ade-183">Minimum supported client</span></span><br/> | <span data-ttu-id="83ade-184">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="83ade-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="83ade-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83ade-185">Minimum supported server</span></span><br/> | <span data-ttu-id="83ade-186">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="83ade-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83ade-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83ade-187">Namespace</span></span><br/>                | <span data-ttu-id="83ade-188">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="83ade-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83ade-189">MOF</span><span class="sxs-lookup"><span data-stu-id="83ade-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83ade-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83ade-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83ade-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83ade-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83ade-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83ade-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

