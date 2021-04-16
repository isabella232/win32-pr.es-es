---
description: Registra un servicio que proporciona objetos relacionados con recursos específicos de la máquina virtual.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540275"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="470fd-103">MSVM \_ VirtualSystemResourceRegistration (clase)</span><span class="sxs-lookup"><span data-stu-id="470fd-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="470fd-104">Registra un servicio que proporciona objetos relacionados con recursos específicos de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="470fd-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="470fd-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="470fd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="470fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="470fd-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="470fd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="470fd-107">Members</span></span>

<span data-ttu-id="470fd-108">La clase **MSVM \_ VirtualSystemResourceRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="470fd-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="470fd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="470fd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="470fd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="470fd-110">Properties</span></span>

<span data-ttu-id="470fd-111">La clase **MSVM \_ VirtualSystemResourceRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="470fd-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="470fd-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="470fd-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470fd-113">Tipo de datos: **[ **MSVM \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="470fd-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="470fd-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="470fd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470fd-115">Referencia a una instancia de que describe el objeto COM que implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="470fd-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="470fd-116">**IsRootDevice**</span><span class="sxs-lookup"><span data-stu-id="470fd-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470fd-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="470fd-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470fd-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="470fd-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470fd-119">**True** si este registro indica si el tipo de recurso especificado es el dispositivo raíz (o el primario menos) para este servicio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="470fd-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="470fd-120">Solo puede existir un registro cuando **IsRootDevice** está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="470fd-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="470fd-121">De lo contrario, este registro representa una asignación a un subdispositivo.</span><span class="sxs-lookup"><span data-stu-id="470fd-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="470fd-122">Esta propiedad siempre se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="470fd-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="470fd-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="470fd-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470fd-124">Tipo de datos: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="470fd-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="470fd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="470fd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470fd-126">Referencia a una instancia de que describe un tipo de recurso admitido por el servicio.</span><span class="sxs-lookup"><span data-stu-id="470fd-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="470fd-127">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="470fd-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="470fd-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="470fd-128">Remarks</span></span>

<span data-ttu-id="470fd-129">El acceso a la clase **MSVM \_ VirtualSystemResourceRegistration** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="470fd-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="470fd-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="470fd-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="470fd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="470fd-131">Requirements</span></span>



| <span data-ttu-id="470fd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="470fd-132">Requirement</span></span> | <span data-ttu-id="470fd-133">Value</span><span class="sxs-lookup"><span data-stu-id="470fd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470fd-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="470fd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="470fd-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="470fd-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="470fd-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="470fd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="470fd-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="470fd-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="470fd-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="470fd-138">End of client support</span></span><br/>    | <span data-ttu-id="470fd-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="470fd-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="470fd-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="470fd-140">End of server support</span></span><br/>    | <span data-ttu-id="470fd-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="470fd-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="470fd-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="470fd-142">Namespace</span></span><br/>                | <span data-ttu-id="470fd-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="470fd-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="470fd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="470fd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="470fd-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="470fd-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="470fd-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="470fd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="470fd-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="470fd-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="470fd-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="470fd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470fd-149">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="470fd-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="470fd-150">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="470fd-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

