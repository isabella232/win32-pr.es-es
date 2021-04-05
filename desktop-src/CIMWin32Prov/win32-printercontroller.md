---
description: La \_ clase WMI PrinterController Association de Win32 relaciona una impresora y el dispositivo local al que está conectada la impresora. Tenga en cuenta que esta clase solo devuelve instancias para las impresoras locales.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907255"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="a74a6-104">\_Clase Win32 PrinterController</span><span class="sxs-lookup"><span data-stu-id="a74a6-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="a74a6-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterController** Association de Win32 relaciona una impresora y el dispositivo local al que está conectada la impresora.</span><span class="sxs-lookup"><span data-stu-id="a74a6-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="a74a6-106">Tenga en cuenta que esta clase solo devuelve instancias para las impresoras locales.</span><span class="sxs-lookup"><span data-stu-id="a74a6-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="a74a6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a74a6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a74a6-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a74a6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74a6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a74a6-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="a74a6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a74a6-110">Members</span></span>

<span data-ttu-id="a74a6-111">La **clase \_ PrinterController de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a74a6-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="a74a6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a74a6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a74a6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a74a6-113">Properties</span></span>

<span data-ttu-id="a74a6-114">La **clase \_ PrinterController de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a74a6-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a74a6-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="a74a6-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a74a6-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-118">Estado del controlador acceso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a74a6-118">State of the controller access to the device.</span></span> <span data-ttu-id="a74a6-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="a74a6-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="a74a6-120">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a74a6-121"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="a74a6-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a74a6-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="a74a6-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a74a6-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a74a6-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a74a6-124">Active</span><span class="sxs-lookup"><span data-stu-id="a74a6-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="a74a6-125"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="a74a6-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="a74a6-126">Inactivo</span><span class="sxs-lookup"><span data-stu-id="a74a6-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a74a6-127">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a74a6-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-128">Tipo de datos **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="a74a6-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-130">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a74a6-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-131">Referencia a la instancia del [**\_ controlador CIM**](cim-controller.md) que representa el dispositivo local asociado a esta impresora.</span><span class="sxs-lookup"><span data-stu-id="a74a6-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="a74a6-132">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="a74a6-133">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a74a6-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-134">Tipo de datos **: \_ impresora Win32**</span><span class="sxs-lookup"><span data-stu-id="a74a6-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-136">Calificadores: [ **clave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a74a6-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-137">Referencia a la instancia de la [**\_ impresora de Win32**](win32-printer.md) que representa la impresora asociada al dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="a74a6-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="a74a6-138">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="a74a6-139">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="a74a6-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a74a6-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-142">Ancho de datos en uso entre dispositivos (cuando son posibles varios anchos de datos de bus o conexión).</span><span class="sxs-lookup"><span data-stu-id="a74a6-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="a74a6-143">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="a74a6-143">Data width is specified in bits.</span></span> <span data-ttu-id="a74a6-144">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="a74a6-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a74a6-145">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="a74a6-146">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="a74a6-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-147">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a74a6-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-149">Velocidad de uso entre dispositivos (cuando se pueden realizar varias velocidades de conexión o bus).</span><span class="sxs-lookup"><span data-stu-id="a74a6-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="a74a6-150">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a74a6-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="a74a6-151">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="a74a6-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a74a6-152">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="a74a6-153">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="a74a6-154">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="a74a6-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a74a6-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-157">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="a74a6-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="a74a6-158">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="a74a6-159">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="a74a6-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a74a6-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a74a6-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a74a6-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74a6-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a74a6-162">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="a74a6-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="a74a6-163">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a74a6-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a74a6-164">Remarks</span></span>

<span data-ttu-id="a74a6-165">La **clase \_ PrinterController de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a74a6-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a74a6-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a74a6-166">Requirements</span></span>



| <span data-ttu-id="a74a6-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="a74a6-167">Requirement</span></span> | <span data-ttu-id="a74a6-168">Value</span><span class="sxs-lookup"><span data-stu-id="a74a6-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a74a6-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a74a6-169">Minimum supported client</span></span><br/> | <span data-ttu-id="a74a6-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a74a6-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a74a6-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a74a6-171">Minimum supported server</span></span><br/> | <span data-ttu-id="a74a6-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a74a6-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a74a6-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a74a6-173">Namespace</span></span><br/>                | <span data-ttu-id="a74a6-174">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a74a6-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a74a6-175">MOF</span><span class="sxs-lookup"><span data-stu-id="a74a6-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a74a6-176"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a74a6-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a74a6-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a74a6-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74a6-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74a6-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a74a6-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="a74a6-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74a6-180">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="a74a6-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="a74a6-181">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="a74a6-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
