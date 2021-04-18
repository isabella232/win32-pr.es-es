---
description: Representa un elemento de grupo de recursos de la plataforma Hyper-V de Microsoft Windows.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652799"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="1fb97-103">MSVM \_ ResourcePoolComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="1fb97-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="1fb97-104">Representa un elemento de grupo de recursos de la plataforma Hyper-V de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1fb97-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="1fb97-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1fb97-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb97-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fb97-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="1fb97-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1fb97-107">Members</span></span>

<span data-ttu-id="1fb97-108">La clase **MSVM \_ ResourcePoolComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1fb97-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1fb97-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fb97-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fb97-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fb97-110">Properties</span></span>

<span data-ttu-id="1fb97-111">La clase **MSVM \_ ResourcePoolComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1fb97-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fb97-112">**AllocationCapabilitiesClassName**</span><span class="sxs-lookup"><span data-stu-id="1fb97-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-115">Nombre de la clase derivada de [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) que describe las capacidades de asignación de este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb97-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-116">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="1fb97-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-119">**GUID** que representa el identificador de clase del objeto com del servicio.</span><span class="sxs-lookup"><span data-stu-id="1fb97-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="1fb97-120">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1fb97-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-121">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="1fb97-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fb97-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-124">Contexto en el que se ejecutará el objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="1fb97-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="1fb97-125">Este valor se pasa en el parámetro *dwClsContext* a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1fb97-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="1fb97-126">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="1fb97-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="1fb97-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1fb97-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-130">**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1fb97-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="1fb97-131">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="1fb97-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-132">**MaxParentPools**</span><span class="sxs-lookup"><span data-stu-id="1fb97-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-133">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1fb97-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-135">El número máximo de grupos de recursos primarios que admite un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="1fb97-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-136">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1fb97-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-139">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="1fb97-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-140">Cadena independiente del lenguaje que identifica de forma única el elemento.</span><span class="sxs-lookup"><span data-stu-id="1fb97-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="1fb97-141">Se sugiere el siguiente formato para evitar conflictos de nomenclatura: " \| versión del componente del proveedor \| ".</span><span class="sxs-lookup"><span data-stu-id="1fb97-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="1fb97-142">Por ejemplo, este nombre representa la versión 1,0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="1fb97-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="1fb97-143">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1fb97-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-144">**PhysicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="1fb97-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-147">Nombre de la clase derivada de un [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa el dispositivo físico desde el que este grupo asigna recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb97-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="1fb97-148">Esta propiedad puede ser **null** si la clase de dispositivo virtual asignada a partir de este grupo es la misma que la clase de dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="1fb97-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-149">**ResourcePoolClassName**</span><span class="sxs-lookup"><span data-stu-id="1fb97-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-152">Nombre de la clase derivada de [**\_ ResourcePool de CIM**](/previous-versions//cc136903(v=vs.85)) que implementa el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb97-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-153">**ResourcePoolSettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="1fb97-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-156">Nombre de la clase derivada del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) que describe la configuración relacionada con la no asignación del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb97-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1fb97-157">**WmiFactoryCLSID**</span><span class="sxs-lookup"><span data-stu-id="1fb97-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb97-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fb97-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fb97-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fb97-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fb97-160">**GUID** que representa el identificador de clase del generador de objetos WMI del componente.</span><span class="sxs-lookup"><span data-stu-id="1fb97-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fb97-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fb97-161">Remarks</span></span>

<span data-ttu-id="1fb97-162">El acceso a la clase **MSVM \_ ResourcePoolComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="1fb97-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1fb97-163">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1fb97-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb97-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb97-164">Requirements</span></span>



| <span data-ttu-id="1fb97-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb97-165">Requirement</span></span> | <span data-ttu-id="1fb97-166">Value</span><span class="sxs-lookup"><span data-stu-id="1fb97-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb97-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb97-167">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb97-168">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb97-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1fb97-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb97-169">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb97-170">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb97-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fb97-171">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1fb97-171">End of client support</span></span><br/>    | <span data-ttu-id="1fb97-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1fb97-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1fb97-173">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1fb97-173">End of server support</span></span><br/>    | <span data-ttu-id="1fb97-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1fb97-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1fb97-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fb97-175">Namespace</span></span><br/>                | <span data-ttu-id="1fb97-176">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1fb97-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1fb97-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1fb97-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fb97-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fb97-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fb97-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1fb97-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb97-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1fb97-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1fb97-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fb97-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb97-182">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="1fb97-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="1fb97-183">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="1fb97-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

