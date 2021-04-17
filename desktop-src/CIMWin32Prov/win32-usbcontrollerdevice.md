---
description: La \_ clase WMI USBControllerDevice Association de Win32 relaciona una controladora de bus serie universal (USB) y la instancia de la plataforma de \_ desconexión de CIM.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659433"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="4ec3d-103">\_Clase Win32 USBControllerDevice</span><span class="sxs-lookup"><span data-stu-id="4ec3d-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="4ec3d-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ USBControllerDevice** Association de Win32 relaciona una controladora de bus serie universal (USB) y la instancia de la plataforma de desconexión de [**CIM \_**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec3d-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="4ec3d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4ec3d-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec3d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ec3d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4ec3d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ec3d-108">Members</span></span>

<span data-ttu-id="4ec3d-109">La **clase \_ USBControllerDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4ec3d-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4ec3d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ec3d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ec3d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ec3d-111">Properties</span></span>

<span data-ttu-id="4ec3d-112">La **clase \_ USBControllerDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ec3d-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-116">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="4ec3d-117">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="4ec3d-118">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ec3d-119">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4ec3d-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4ec3d-120">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="4ec3d-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4ec3d-121">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="4ec3d-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ec3d-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-123">Tipo de datos: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-125">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ USBController")</span><span class="sxs-lookup"><span data-stu-id="4ec3d-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-126">Un [**\_ USBController de CIM**](cim-usbcontroller.md) que representa el controlador de bus serie universal (USB) asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="4ec3d-127">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-128">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-130">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="4ec3d-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-131">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico conectado al controlador de bus serie universal (USB).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="4ec3d-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-135">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="4ec3d-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-136">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="4ec3d-137">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-137">Data width is specified in bits.</span></span> <span data-ttu-id="4ec3d-138">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ec3d-139">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec3d-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-143">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="4ec3d-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-144">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="4ec3d-145">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="4ec3d-146">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ec3d-147">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="4ec3d-148">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec3d-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-152">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="4ec3d-153">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="4ec3d-154">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="4ec3d-155">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec3d-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec3d-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec3d-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec3d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ec3d-159">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="4ec3d-160">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="4ec3d-161">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="4ec3d-162">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ec3d-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ec3d-163">Remarks</span></span>

<span data-ttu-id="4ec3d-164">La **clase \_ USBControllerDevice de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3d-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="4ec3d-165">Para obtener una explicación sobre el uso de, consulte el artículo [visualización de dispositivos USB con](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) el blog de WMI.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="4ec3d-166">Para obtener una explicación sobre el uso de las clases de asociación, consulte el artículo [Get-USB-Using WMI Association classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4ec3d-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="4ec3d-167">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4ec3d-167">Examples</span></span>

<span data-ttu-id="4ec3d-168">En el siguiente ejemplo de PowerShell se recupera el dispositivo lógico dependiente y se muestra la información pertinente.</span><span class="sxs-lookup"><span data-stu-id="4ec3d-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="4ec3d-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ec3d-169">Requirements</span></span>



| <span data-ttu-id="4ec3d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec3d-170">Requirement</span></span> | <span data-ttu-id="4ec3d-171">Value</span><span class="sxs-lookup"><span data-stu-id="4ec3d-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec3d-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ec3d-172">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec3d-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ec3d-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ec3d-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ec3d-174">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec3d-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ec3d-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ec3d-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ec3d-176">Namespace</span></span><br/>                | <span data-ttu-id="4ec3d-177">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4ec3d-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ec3d-178">MOF</span><span class="sxs-lookup"><span data-stu-id="4ec3d-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ec3d-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3d-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ec3d-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ec3d-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec3d-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3d-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec3d-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ec3d-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec3d-183">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="4ec3d-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="4ec3d-184">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="4ec3d-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
