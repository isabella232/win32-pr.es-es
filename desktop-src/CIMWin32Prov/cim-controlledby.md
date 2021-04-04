---
description: La relación de ControlledBy de CIM indica los dispositivos a los \_ que se puede acceder o a los que se accede mediante el dispositivo lógico del controlador.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: CIM_ControlledBy (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907182"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="ed694-103">CIM_ControlledBy (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ed694-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ed694-104">La relación de **\_ ControlledBy de CIM** indica los dispositivos a los que se puede acceder o a los que se accede mediante el dispositivo lógico del controlador.</span><span class="sxs-lookup"><span data-stu-id="ed694-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed694-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ed694-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ed694-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ed694-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ed694-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ed694-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ed694-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ed694-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed694-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed694-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="ed694-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed694-110">Members</span></span>

<span data-ttu-id="ed694-111">La clase **CIM \_ ControlledBy** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ed694-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="ed694-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed694-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed694-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed694-113">Properties</span></span>

<span data-ttu-id="ed694-114">La clase **CIM \_ ControlledBy** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed694-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed694-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="ed694-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed694-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed694-118">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed694-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="ed694-119">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="ed694-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed694-120">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ed694-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ed694-121">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="ed694-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ed694-122">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="ed694-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed694-123">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ed694-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-124">Tipo de datos **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="ed694-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed694-126">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ed694-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ed694-127">Un [**\_ controlador CIM**](cim-controller.md) que representa el controlador.</span><span class="sxs-lookup"><span data-stu-id="ed694-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="ed694-128">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="ed694-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-129">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="ed694-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed694-131">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="ed694-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ed694-132">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa el dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="ed694-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="ed694-133">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="ed694-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed694-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed694-136">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="ed694-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ed694-137">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ed694-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="ed694-138">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="ed694-138">Data width is specified in bits.</span></span> <span data-ttu-id="ed694-139">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ed694-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ed694-140">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ed694-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed694-141">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ed694-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-142">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed694-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed694-144">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="ed694-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="ed694-145">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ed694-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="ed694-146">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ed694-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="ed694-147">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ed694-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ed694-148">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ed694-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ed694-149">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ed694-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed694-150">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="ed694-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed694-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed694-153">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="ed694-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="ed694-154">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="ed694-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="ed694-155">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="ed694-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="ed694-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="ed694-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed694-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed694-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed694-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed694-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed694-159">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="ed694-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="ed694-160">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="ed694-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="ed694-161">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="ed694-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed694-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed694-162">Remarks</span></span>

<span data-ttu-id="ed694-163">La clase **CIM \_ ControlledBy** se deriva de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ed694-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="ed694-164">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ed694-164">WMI does not implement this class.</span></span> <span data-ttu-id="ed694-165">Para obtener más información sobre las clases derivadas de **CIM \_ ControlledBy**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ed694-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ed694-166">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ed694-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ed694-167">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ed694-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed694-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed694-168">Requirements</span></span>



| <span data-ttu-id="ed694-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed694-169">Requirement</span></span> | <span data-ttu-id="ed694-170">Value</span><span class="sxs-lookup"><span data-stu-id="ed694-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed694-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed694-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ed694-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed694-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed694-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed694-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ed694-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed694-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed694-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed694-175">Namespace</span></span><br/>                | <span data-ttu-id="ed694-176">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ed694-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed694-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ed694-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed694-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed694-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed694-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed694-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed694-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed694-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed694-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed694-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed694-182">**DeviceConnection de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ed694-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

