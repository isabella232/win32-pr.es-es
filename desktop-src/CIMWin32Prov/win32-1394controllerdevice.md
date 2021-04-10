---
description: La \_ clase WMI 1394ControllerDevice Association de Win32 relaciona el controlador de bus serie de alta velocidad (IEEE 1394 FireWire) y la instancia de LogicalDevice de CIM \_ conectada a él.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Win32_1394ControllerDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907463"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="9f4d2-103">\_Clase Win32 1394ControllerDevice</span><span class="sxs-lookup"><span data-stu-id="9f4d2-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="9f4d2-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ 1394ControllerDevice** Association de Win32 relaciona el controlador de bus serie de alta velocidad (IEEE 1394 FireWire) y la instancia de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) conectada a él.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="9f4d2-105">Este bus serie proporciona conectividad mejorada para una amplia gama de dispositivos, incluidos componentes de audio o vídeo de consumidor, periféricos de almacenamiento, otros equipos y dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="9f4d2-106">La industria de electrónica del consumidor ha adoptado IEEE 1394 y proporciona una interfaz de expansión compatible con Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="9f4d2-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9f4d2-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4d2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f4d2-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9f4d2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f4d2-110">Members</span></span>

<span data-ttu-id="9f4d2-111">La **clase \_ 1394ControllerDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f4d2-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="9f4d2-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4d2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f4d2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4d2-113">Properties</span></span>

<span data-ttu-id="9f4d2-114">La **clase \_ 1394ControllerDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f4d2-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-118">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="9f4d2-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="9f4d2-120">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f4d2-121">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9f4d2-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="9f4d2-122">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="9f4d2-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="9f4d2-123">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="9f4d2-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f4d2-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-125">Tipo de datos: **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")</span><span class="sxs-lookup"><span data-stu-id="9f4d2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-128">La \_ referencia antecedente 1394Controller de Win32 representa el controlador 1394 asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d2-129">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-130">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-132">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="9f4d2-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-133">La \_ referencia dependiente del logicaldevice de CIM representa el LogicalDevice de CIM \_ conectado al controlador 1394.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d2-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-137">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="9f4d2-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-138">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="9f4d2-139">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-139">Data width is specified in bits.</span></span> <span data-ttu-id="9f4d2-140">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="9f4d2-141">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f4d2-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-145">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="9f4d2-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-146">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="9f4d2-147">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="9f4d2-148">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="9f4d2-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9f4d2-150">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f4d2-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-154">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="9f4d2-155">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="9f4d2-156">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="9f4d2-157">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f4d2-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d2-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d2-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d2-161">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="9f4d2-162">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="9f4d2-163">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="9f4d2-164">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f4d2-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f4d2-165">Remarks</span></span>

<span data-ttu-id="9f4d2-166">La **clase \_ 1394ControllerDevice de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d2-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9f4d2-167">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f4d2-167">Examples</span></span>

<span data-ttu-id="9f4d2-168">El siguiente ejemplo de código de PowerShell recupera información del dispositivo del controlador 1394.</span><span class="sxs-lookup"><span data-stu-id="9f4d2-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="9f4d2-169">El ejemplo de código anterior devuelve la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="9f4d2-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="9f4d2-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f4d2-170">Requirements</span></span>



| <span data-ttu-id="9f4d2-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f4d2-171">Requirement</span></span> | <span data-ttu-id="9f4d2-172">Value</span><span class="sxs-lookup"><span data-stu-id="9f4d2-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4d2-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4d2-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4d2-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f4d2-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f4d2-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4d2-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4d2-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f4d2-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f4d2-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f4d2-177">Namespace</span></span><br/>                | <span data-ttu-id="9f4d2-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9f4d2-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f4d2-179">MOF</span><span class="sxs-lookup"><span data-stu-id="9f4d2-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f4d2-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f4d2-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f4d2-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f4d2-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f4d2-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f4d2-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f4d2-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f4d2-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4d2-184">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="9f4d2-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="9f4d2-185">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9f4d2-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

