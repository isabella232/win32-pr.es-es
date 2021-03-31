---
description: Representa una relación de ControlledBy de CIM \_ que indica a qué dispositivos se tiene acceso a través de una controladora SCSI y las características de acceso.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: CIM_SCSIInterface (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807597"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="4edb7-103">\_Clase SCSIInterface de CIM</span><span class="sxs-lookup"><span data-stu-id="4edb7-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="4edb7-104">La clase **CIM \_ SCSIInterface** representa una relación [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través de una controladora SCSI y las características de acceso.</span><span class="sxs-lookup"><span data-stu-id="4edb7-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4edb7-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4edb7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4edb7-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4edb7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4edb7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4edb7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4edb7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4edb7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4edb7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4edb7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="4edb7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4edb7-110">Members</span></span>

<span data-ttu-id="4edb7-111">La clase **CIM \_ SCSIInterface** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4edb7-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="4edb7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4edb7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4edb7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4edb7-113">Properties</span></span>

<span data-ttu-id="4edb7-114">La clase **CIM \_ SCSIInterface** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4edb7-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4edb7-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="4edb7-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edb7-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-118">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4edb7-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="4edb7-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="4edb7-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="4edb7-120">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4edb7-121">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4edb7-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4edb7-122">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="4edb7-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4edb7-123">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="4edb7-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4edb7-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4edb7-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-125">Tipo de datos: **CIM \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="4edb7-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-127">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="4edb7-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-128">Un [**\_ SCSIController de CIM**](cim-scsicontroller.md) que describe el controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="4edb7-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-129">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4edb7-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-130">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="4edb7-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-132">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="4edb7-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-133">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4edb7-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="4edb7-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4edb7-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-137">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="4edb7-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-138">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4edb7-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="4edb7-139">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="4edb7-139">Data width is specified in bits.</span></span> <span data-ttu-id="4edb7-140">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4edb7-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4edb7-141">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4edb7-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4edb7-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-145">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="4edb7-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-146">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4edb7-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="4edb7-147">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4edb7-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="4edb7-148">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4edb7-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4edb7-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4edb7-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4edb7-150">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="4edb7-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4edb7-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-154">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4edb7-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="4edb7-155">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="4edb7-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="4edb7-156">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="4edb7-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="4edb7-157">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="4edb7-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4edb7-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-161">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4edb7-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="4edb7-162">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="4edb7-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="4edb7-163">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="4edb7-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="4edb7-164">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-165">**SCSIRetries**</span><span class="sxs-lookup"><span data-stu-id="4edb7-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4edb7-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-168">Número de reintentos SCSI que se han producido desde la última vez que se reinició el hardware o el dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="4edb7-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="4edb7-169">La hora del último restablecimiento se indica en la propiedad **TimeOfDeviceReset** , heredada de la [**Asociación \_ ControlledBy de CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="4edb7-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="4edb7-170">**SCSITimeouts**</span><span class="sxs-lookup"><span data-stu-id="4edb7-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edb7-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4edb7-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4edb7-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4edb7-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edb7-173">Número de tiempos de espera SCSI que se produjeron desde el último restablecimiento de hardware o software relacionado con el dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="4edb7-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="4edb7-174">La hora del último restablecimiento se indica en la propiedad **TimeOfDeviceReset** , heredada de la [**Asociación \_ ControlledBy de CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="4edb7-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4edb7-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4edb7-175">Remarks</span></span>

<span data-ttu-id="4edb7-176">La clase **CIM \_ SCSIInterface** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4edb7-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="4edb7-177">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="4edb7-177">WMI does not implement this class.</span></span>

<span data-ttu-id="4edb7-178">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4edb7-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4edb7-179">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4edb7-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4edb7-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4edb7-180">Requirements</span></span>



| <span data-ttu-id="4edb7-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="4edb7-181">Requirement</span></span> | <span data-ttu-id="4edb7-182">Value</span><span class="sxs-lookup"><span data-stu-id="4edb7-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4edb7-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4edb7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4edb7-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4edb7-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4edb7-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4edb7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4edb7-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4edb7-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4edb7-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4edb7-187">Namespace</span></span><br/>                | <span data-ttu-id="4edb7-188">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4edb7-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4edb7-189">MOF</span><span class="sxs-lookup"><span data-stu-id="4edb7-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4edb7-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4edb7-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4edb7-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4edb7-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4edb7-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4edb7-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4edb7-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="4edb7-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edb7-194">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="4edb7-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

