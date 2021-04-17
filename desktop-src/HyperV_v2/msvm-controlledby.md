---
description: Asocia un dispositivo de almacenamiento con el controlador de almacenamiento que posee el dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688363"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="1a50a-103">MSVM \_ ControlledBy (clase)</span><span class="sxs-lookup"><span data-stu-id="1a50a-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="1a50a-104">Asocia un dispositivo de almacenamiento con el controlador de almacenamiento que posee el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a50a-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="1a50a-105">Esta asociación se usa con ambos controladores IDE y de disquete.</span><span class="sxs-lookup"><span data-stu-id="1a50a-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="1a50a-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a50a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a50a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a50a-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="1a50a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a50a-108">Members</span></span>

<span data-ttu-id="1a50a-109">La clase **MSVM \_ ControlledBy** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a50a-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="1a50a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a50a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a50a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a50a-111">Properties</span></span>

<span data-ttu-id="1a50a-112">La clase **MSVM \_ ControlledBy** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a50a-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a50a-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="1a50a-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a50a-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-116">Accesibilidad del dispositivo a través del controlador antecedente.</span><span class="sxs-lookup"><span data-stu-id="1a50a-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="1a50a-117">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre está establecida en 2 (lectura y escritura).</span><span class="sxs-lookup"><span data-stu-id="1a50a-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="1a50a-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a50a-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-121">La prioridad dada para acceder al dispositivo a través de este controlador.</span><span class="sxs-lookup"><span data-stu-id="1a50a-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="1a50a-122">La ruta de acceso de prioridad más alta tendrá el valor más bajo.</span><span class="sxs-lookup"><span data-stu-id="1a50a-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="1a50a-123">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="1a50a-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-124">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="1a50a-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a50a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-127">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a50a-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="1a50a-128">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)y siempre está establecida en 1 (activo).</span><span class="sxs-lookup"><span data-stu-id="1a50a-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-129">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1a50a-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-130">Tipo de datos: **[ **\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="1a50a-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-132">Referencia al controlador.</span><span class="sxs-lookup"><span data-stu-id="1a50a-132">A reference to the controller.</span></span> <span data-ttu-id="1a50a-133">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="1a50a-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-134">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1a50a-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-135">Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="1a50a-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-137">Referencia al dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="1a50a-137">A reference to the controlled device.</span></span> <span data-ttu-id="1a50a-138">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="1a50a-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-139">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="1a50a-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a50a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-142">La dirección del dispositivo asociado en el contexto del controlador antecedente.</span><span class="sxs-lookup"><span data-stu-id="1a50a-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="1a50a-143">Esta propiedad se hereda de [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="1a50a-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-144">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="1a50a-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a50a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-147">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="1a50a-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-148">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1a50a-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-149">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a50a-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-151">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="1a50a-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-152">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="1a50a-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a50a-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-155">Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="1a50a-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="1a50a-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a50a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-159">Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="1a50a-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a50a-160">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="1a50a-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a50a-161">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a50a-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a50a-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a50a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a50a-163">Esta propiedad se hereda de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="1a50a-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a50a-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a50a-164">Remarks</span></span>

<span data-ttu-id="1a50a-165">El acceso a la clase **MSVM \_ ControlledBy** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="1a50a-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1a50a-166">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1a50a-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a50a-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a50a-167">Requirements</span></span>



| <span data-ttu-id="1a50a-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a50a-168">Requirement</span></span> | <span data-ttu-id="1a50a-169">Value</span><span class="sxs-lookup"><span data-stu-id="1a50a-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a50a-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a50a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1a50a-171">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a50a-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1a50a-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a50a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1a50a-173">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a50a-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a50a-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a50a-174">Namespace</span></span><br/>                | <span data-ttu-id="1a50a-175">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1a50a-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1a50a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1a50a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a50a-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a50a-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a50a-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a50a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a50a-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a50a-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a50a-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a50a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a50a-181">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="1a50a-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="1a50a-182">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="1a50a-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="1a50a-183">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="1a50a-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

