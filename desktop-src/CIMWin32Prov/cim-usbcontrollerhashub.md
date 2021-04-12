---
description: La \_ clase CIM USBControllerHasHub define los concentradores que son inferiores al controlador USB.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: CIM_USBControllerHasHub (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152771"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="ddb01-103">\_Clase USBControllerHasHub de CIM</span><span class="sxs-lookup"><span data-stu-id="ddb01-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="ddb01-104">La clase **CIM \_ USBControllerHasHub** define los concentradores que son inferiores al controlador USB.</span><span class="sxs-lookup"><span data-stu-id="ddb01-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ddb01-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ddb01-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ddb01-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ddb01-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ddb01-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ddb01-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ddb01-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ddb01-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb01-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddb01-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ddb01-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddb01-110">Members</span></span>

<span data-ttu-id="ddb01-111">La clase **CIM \_ USBControllerHasHub** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ddb01-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="ddb01-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddb01-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddb01-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddb01-113">Properties</span></span>

<span data-ttu-id="ddb01-114">La clase **CIM \_ USBControllerHasHub** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ddb01-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddb01-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="ddb01-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddb01-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-118">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddb01-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="ddb01-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="ddb01-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="ddb01-120">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddb01-121">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb01-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ddb01-122">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="ddb01-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ddb01-123">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="ddb01-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb01-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ddb01-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-125">Tipo de datos: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="ddb01-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-127">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ddb01-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-128">Un [**\_ USBController de CIM**](cim-usbcontroller.md) que describe el USBController.</span><span class="sxs-lookup"><span data-stu-id="ddb01-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="ddb01-129">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="ddb01-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-130">Tipo de datos **: \_ Hub de CIM**</span><span class="sxs-lookup"><span data-stu-id="ddb01-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-132">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="ddb01-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-133">Un [**\_ USBHUB de CIM**](cim-usbhub.md) que describe el USBHUB que está asociado con el controlador.</span><span class="sxs-lookup"><span data-stu-id="ddb01-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="ddb01-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="ddb01-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb01-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-137">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="ddb01-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-138">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ddb01-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="ddb01-139">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="ddb01-139">Data width is specified in bits.</span></span> <span data-ttu-id="ddb01-140">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ddb01-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ddb01-141">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb01-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ddb01-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddb01-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-145">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="ddb01-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-146">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ddb01-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="ddb01-147">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ddb01-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="ddb01-148">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ddb01-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ddb01-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ddb01-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ddb01-150">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb01-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="ddb01-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb01-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-154">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="ddb01-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="ddb01-155">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="ddb01-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="ddb01-156">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="ddb01-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="ddb01-157">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb01-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="ddb01-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb01-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb01-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb01-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb01-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb01-161">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="ddb01-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="ddb01-162">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="ddb01-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="ddb01-163">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="ddb01-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="ddb01-164">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddb01-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddb01-165">Remarks</span></span>

<span data-ttu-id="ddb01-166">La clase **CIM \_ USBControllerHasHub** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="ddb01-167">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ddb01-167">WMI does not implement this class.</span></span> <span data-ttu-id="ddb01-168">Para las clases WMI derivadas de **CIM \_ USBControllerHasHub**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ddb01-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ddb01-169">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ddb01-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ddb01-170">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ddb01-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb01-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb01-171">Requirements</span></span>



| <span data-ttu-id="ddb01-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb01-172">Requirement</span></span> | <span data-ttu-id="ddb01-173">Value</span><span class="sxs-lookup"><span data-stu-id="ddb01-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb01-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb01-174">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb01-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb01-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddb01-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb01-176">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb01-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb01-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddb01-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddb01-178">Namespace</span></span><br/>                | <span data-ttu-id="ddb01-179">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ddb01-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddb01-180">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb01-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb01-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddb01-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb01-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddb01-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb01-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb01-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb01-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb01-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb01-185">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="ddb01-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

