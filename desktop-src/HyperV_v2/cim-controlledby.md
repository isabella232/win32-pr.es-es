---
description: Representa una relación entre un controlador y un dispositivo lógico administrado por el controlador.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: CIM_ControlledBy (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908229"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="3def0-103">CIM_ControlledBy (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="3def0-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="3def0-104">Representa una relación entre un controlador y un dispositivo lógico administrado por el controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="3def0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3def0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="3def0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3def0-106">Members</span></span>

<span data-ttu-id="3def0-107">La clase **CIM \_ ControlledBy** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3def0-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="3def0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3def0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3def0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3def0-109">Properties</span></span>

<span data-ttu-id="3def0-110">La clase **CIM \_ ControlledBy** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3def0-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3def0-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="3def0-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3def0-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3def0-114">Esta propiedad describe la accesibilidad del dispositivo a través del controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="3def0-115">**ReadWrite** (2)</span><span class="sxs-lookup"><span data-stu-id="3def0-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="3def0-116">**ReadOnly** (3)</span><span class="sxs-lookup"><span data-stu-id="3def0-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="3def0-117">**NoAccess** (4)</span><span class="sxs-lookup"><span data-stu-id="3def0-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3def0-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="3def0-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3def0-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3def0-121">La prioridad para el acceso del dispositivo a través del controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="3def0-122">Un valor inferior indica una prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="3def0-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-123">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="3def0-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3def0-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3def0-126">Indica si el controlador está administrando activamente el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3def0-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3def0-127">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3def0-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="3def0-128">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="3def0-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="3def0-129">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="3def0-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3def0-130">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3def0-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-131">Tipo de datos **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="3def0-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3def0-133">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3def0-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3def0-134">Controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-135">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3def0-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-136">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="3def0-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3def0-138">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="3def0-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3def0-139">Los dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="3def0-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-140">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="3def0-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3def0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3def0-143">La dirección del dispositivo asociado en el contexto del controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-144">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="3def0-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3def0-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3def0-147">Calificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="3def0-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="3def0-148">El número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="3def0-149">Un restablecimiento de hardware devuelve un dispositivo a su estado de inicialización o arranque, después del cual se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="3def0-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-150">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="3def0-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3def0-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3def0-153">Calificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="3def0-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="3def0-154">El número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="3def0-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="3def0-155">Un restablecimiento parcial no borra el estado o los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3def0-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="3def0-156">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="3def0-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3def0-157">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3def0-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3def0-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3def0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3def0-159">La hora a la que el controlador restableció por última vez el dispositivo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="3def0-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3def0-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3def0-160">Requirements</span></span>



| <span data-ttu-id="3def0-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="3def0-161">Requirement</span></span> | <span data-ttu-id="3def0-162">Value</span><span class="sxs-lookup"><span data-stu-id="3def0-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3def0-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3def0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="3def0-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3def0-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3def0-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3def0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="3def0-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3def0-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3def0-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3def0-167">Namespace</span></span><br/>                | <span data-ttu-id="3def0-168">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3def0-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3def0-169">MOF</span><span class="sxs-lookup"><span data-stu-id="3def0-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3def0-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3def0-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3def0-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3def0-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3def0-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3def0-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3def0-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="3def0-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3def0-174">**DeviceConnection de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3def0-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

