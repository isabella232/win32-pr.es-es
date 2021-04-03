---
description: Representa un evento que se genera cada vez que cambia la propiedad OperationalStatus de la \_ clase MSVM ResourcePool o MSVM \_ LogicalDisk.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082938"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="627b5-103">MSVM \_ StorageAlert (clase)</span><span class="sxs-lookup"><span data-stu-id="627b5-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="627b5-104">Representa un evento que se genera cada vez que cambia la propiedad **OperationalStatus** de la clase [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) .</span><span class="sxs-lookup"><span data-stu-id="627b5-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="627b5-105">La siguiente sintaxis se simplifica desde el código MOF e incluye estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="627b5-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="627b5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="627b5-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="627b5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="627b5-107">Members</span></span>

<span data-ttu-id="627b5-108">La clase **MSVM \_ StorageAlert** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="627b5-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="627b5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="627b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="627b5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="627b5-110">Properties</span></span>

<span data-ttu-id="627b5-111">La clase **MSVM \_ StorageAlert** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="627b5-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="627b5-112">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="627b5-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="627b5-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="627b5-115">Calificadores: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")</span><span class="sxs-lookup"><span data-stu-id="627b5-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="627b5-116">Especifica el formato de la propiedad **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="627b5-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="627b5-117">El formato es CIMObjectPath, con el formato *<NamespacePath> : <ClassName> "" <Prop1> = \\ <Value1> \\ , " <Prop2> = \\ " <Value2> \\ "*, que especifica una instancia en el esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="627b5-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="627b5-118">Esta propiedad se hereda de la **clase \_ AlertIndication de CIM** .</span><span class="sxs-lookup"><span data-stu-id="627b5-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="627b5-119">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="627b5-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="627b5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="627b5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="627b5-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="627b5-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="627b5-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="627b5-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="627b5-123">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="627b5-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-124">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="627b5-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="627b5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-126">Las rutas de acceso WMI de la instancia para la que se genera la alerta.</span><span class="sxs-lookup"><span data-stu-id="627b5-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="627b5-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="627b5-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="627b5-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-130">Especifica la clasificación principal de la alerta.</span><span class="sxs-lookup"><span data-stu-id="627b5-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="627b5-131">Los posibles valores para esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="627b5-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="627b5-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de calidad de servicio** (3)</span><span class="sxs-lookup"><span data-stu-id="627b5-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="627b5-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="627b5-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-134">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="627b5-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-136">Fecha y hora en que se detectó el evento subyacente.</span><span class="sxs-lookup"><span data-stu-id="627b5-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="627b5-137">**Message**</span><span class="sxs-lookup"><span data-stu-id="627b5-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="627b5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-140">Un mensaje con formato que se construye combinando algunos o todos los elementos dinámicos que se especifican en la propiedad **MessageArguments** con los elementos estáticos identificados de forma exclusiva por la propiedad **MessageID** en un registro de mensajes u otro Catálogo asociado a la propiedad **OwningEntity** .</span><span class="sxs-lookup"><span data-stu-id="627b5-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="627b5-141">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="627b5-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-142">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="627b5-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="627b5-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-144">Una matriz que contiene el contenido dinámico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="627b5-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="627b5-145">Si el valor de **MessageID** es 32930, el argumento de la posición 0 es el **PoolID** de la instancia de [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) para el que se genera la alerta.</span><span class="sxs-lookup"><span data-stu-id="627b5-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="627b5-146">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="627b5-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="627b5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-149">Identifica de forma única, dentro del ámbito de la propiedad **OwningEntity** , el formato de la propiedad de **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="627b5-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="627b5-150">Los posibles valores para esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="627b5-150">The possible values for this property are:</span></span>

<span data-ttu-id="627b5-151">32930 ("mensaje de rendimiento insuficiente de QoS del bloque de almacenamiento")</span><span class="sxs-lookup"><span data-stu-id="627b5-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="627b5-152">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="627b5-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="627b5-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-155">Una cadena que define los "otros" valores para **AlertingManagedElement**.</span><span class="sxs-lookup"><span data-stu-id="627b5-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="627b5-156">Este valor debe establecerse en un valor distinto de NULL cuando **AlertingManagedElement** se establece en un valor de 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="627b5-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="627b5-157">Para todos los demás valores de **AlertingManagedElement**, el valor de esta cadena debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="627b5-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="627b5-158">Esta propiedad se hereda de la **clase \_ AlertIndication de CIM** .</span><span class="sxs-lookup"><span data-stu-id="627b5-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="627b5-159">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="627b5-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="627b5-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-162">Identifica de forma única la entidad propietaria de la definición del formato del **mensaje** descrito en esta instancia.</span><span class="sxs-lookup"><span data-stu-id="627b5-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="627b5-163">El valor de esta propiedad siempre es "Microsoft-Windows-Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="627b5-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="627b5-164">"Microsoft-Windows-Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="627b5-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="627b5-165">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="627b5-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="627b5-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-168">Describe la gravedad de la indicación de alerta.</span><span class="sxs-lookup"><span data-stu-id="627b5-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="627b5-169">Los posibles valores para esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="627b5-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="627b5-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)</span><span class="sxs-lookup"><span data-stu-id="627b5-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="627b5-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)</span><span class="sxs-lookup"><span data-stu-id="627b5-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="627b5-172">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="627b5-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="627b5-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-175">Describe la causa probable de la situación que produjo la indicación de la alerta.</span><span class="sxs-lookup"><span data-stu-id="627b5-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="627b5-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidad de almacenamiento** (50)</span><span class="sxs-lookup"><span data-stu-id="627b5-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="627b5-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior desactivada** (59)</span><span class="sxs-lookup"><span data-stu-id="627b5-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="627b5-178">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="627b5-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="627b5-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="627b5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="627b5-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="627b5-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="627b5-181">Una descripción textual que corresponde al valor de la propiedad **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="627b5-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="627b5-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="627b5-182">Remarks</span></span>

<span data-ttu-id="627b5-183">El proveedor WMI de Hyper-V no genera eventos para discos virtuales individuales a fin de evitar el desbordamiento de clientes con eventos en el caso de las funciones de gran escala de los sistemas de almacenamiento subyacentes.</span><span class="sxs-lookup"><span data-stu-id="627b5-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="627b5-184">Cuando un cliente recibe un evento **MSVM \_ StorageAlert** , si el valor de la propiedad **ProbableCause** es 50 (problema de capacidad de almacenamiento), el cliente puede detectar qué discos virtuales están funcionando fuera de su Directiva de QoS mediante uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="627b5-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="627b5-185">Consulte todas las instancias de [**\_ LogicalDisk de MSVM**](msvm-logicaldisk.md) que se asignaron desde el grupo de recursos para el que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="627b5-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="627b5-186">Estas instancias de **MSVM \_ LogicalDisk** están asociadas al grupo de recursos a través de la Asociación [**\_ ElementAllocatedFromPool de MSVM**](msvm-elementallocatedfrompool.md) .</span><span class="sxs-lookup"><span data-stu-id="627b5-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="627b5-187">Filtre la lista de resultados seleccionando instancias cuyo OperationalStatus contiene un rendimiento insuficiente.</span><span class="sxs-lookup"><span data-stu-id="627b5-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="627b5-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="627b5-188">Requirements</span></span>



| <span data-ttu-id="627b5-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="627b5-189">Requirement</span></span> | <span data-ttu-id="627b5-190">Value</span><span class="sxs-lookup"><span data-stu-id="627b5-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="627b5-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="627b5-191">Minimum supported client</span></span><br/> | <span data-ttu-id="627b5-192">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="627b5-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="627b5-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="627b5-193">Minimum supported server</span></span><br/> | <span data-ttu-id="627b5-194">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="627b5-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="627b5-195">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="627b5-195">Namespace</span></span><br/>                | <span data-ttu-id="627b5-196">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="627b5-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="627b5-197">MOF</span><span class="sxs-lookup"><span data-stu-id="627b5-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="627b5-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="627b5-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="627b5-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="627b5-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="627b5-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="627b5-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="627b5-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="627b5-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627b5-202">**\_ALERTINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="627b5-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="627b5-203">**MSVM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="627b5-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="627b5-204">**MSVM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="627b5-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




