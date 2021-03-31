---
description: La \_ clase WMI IDEControllerDevice Association de Win32 relaciona una controladora IDE (electrónica integrada de unidades) y el dispositivo lógico conectado a, por ejemplo, una unidad de disco.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Win32_IDEControllerDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423467"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="c358b-103">\_Clase Win32 IDEControllerDevice</span><span class="sxs-lookup"><span data-stu-id="c358b-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="c358b-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ IDEControllerDevice** Association de Win32 relaciona una controladora IDE (electrónica integrada de unidades) y el dispositivo lógico conectado a, por ejemplo, una unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="c358b-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="c358b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c358b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c358b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c358b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c358b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c358b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c358b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c358b-108">Members</span></span>

<span data-ttu-id="c358b-109">La **clase \_ IDEControllerDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c358b-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c358b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c358b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c358b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c358b-111">Properties</span></span>

<span data-ttu-id="c358b-112">La **clase \_ IDEControllerDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c358b-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c358b-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="c358b-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c358b-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c358b-116">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c358b-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="c358b-117">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="c358b-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="c358b-118">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c358b-119">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c358b-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="c358b-120">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="c358b-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="c358b-121">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="c358b-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c358b-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c358b-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-123">Tipo de datos: **Win32 \_ IDEController**</span><span class="sxs-lookup"><span data-stu-id="c358b-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c358b-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ IDEController")</span><span class="sxs-lookup"><span data-stu-id="c358b-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="c358b-126">[**\_ IDEController de Win32**](win32-idecontroller.md) que representa la controladora IDE asociada a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c358b-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="c358b-127">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="c358b-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-128">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="c358b-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c358b-130">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="c358b-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="c358b-131">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa el dispositivo lógico conectado a la controladora IDE.</span><span class="sxs-lookup"><span data-stu-id="c358b-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="c358b-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="c358b-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c358b-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c358b-135">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="c358b-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c358b-136">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c358b-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="c358b-137">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="c358b-137">Data width is specified in bits.</span></span> <span data-ttu-id="c358b-138">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c358b-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="c358b-139">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="c358b-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c358b-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c358b-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c358b-143">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="c358b-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="c358b-144">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c358b-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="c358b-145">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c358b-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="c358b-146">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c358b-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="c358b-147">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c358b-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c358b-148">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="c358b-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="c358b-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c358b-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c358b-152">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="c358b-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="c358b-153">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="c358b-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="c358b-154">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="c358b-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="c358b-155">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="c358b-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="c358b-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c358b-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c358b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c358b-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c358b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c358b-159">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="c358b-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="c358b-160">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="c358b-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="c358b-161">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="c358b-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="c358b-162">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c358b-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c358b-163">Remarks</span></span>

<span data-ttu-id="c358b-164">La **clase \_ IDEControllerDevice de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="c358b-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c358b-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c358b-165">Requirements</span></span>



| <span data-ttu-id="c358b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="c358b-166">Requirement</span></span> | <span data-ttu-id="c358b-167">Value</span><span class="sxs-lookup"><span data-stu-id="c358b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c358b-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c358b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c358b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c358b-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c358b-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c358b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c358b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c358b-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c358b-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c358b-172">Namespace</span></span><br/>                | <span data-ttu-id="c358b-173">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c358b-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c358b-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c358b-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c358b-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c358b-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c358b-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c358b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c358b-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c358b-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c358b-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="c358b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c358b-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="c358b-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="c358b-180">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="c358b-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

