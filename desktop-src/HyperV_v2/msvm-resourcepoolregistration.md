---
description: Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156685"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="31781-103">MSVM \_ ResourcePoolRegistration (clase)</span><span class="sxs-lookup"><span data-stu-id="31781-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="31781-104">Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31781-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="31781-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="31781-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31781-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31781-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="31781-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="31781-107">Members</span></span>

<span data-ttu-id="31781-108">La clase **MSVM \_ ResourcePoolRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31781-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="31781-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31781-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31781-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31781-110">Properties</span></span>

<span data-ttu-id="31781-111">La clase **MSVM \_ ResourcePoolRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="31781-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31781-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="31781-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31781-113">Tipo de datos: **[ **MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="31781-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31781-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31781-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31781-115">Referencia a una instancia de que describe el objeto COM que implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="31781-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="31781-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="31781-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31781-117">Tipo de datos: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="31781-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31781-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31781-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31781-119">Referencia a una instancia de que describe un tipo de recurso admitido por el servicio.</span><span class="sxs-lookup"><span data-stu-id="31781-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="31781-120">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="31781-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31781-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31781-121">Remarks</span></span>

<span data-ttu-id="31781-122">El acceso a la clase **MSVM \_ ResourcePoolRegistration** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="31781-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="31781-123">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="31781-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="31781-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31781-124">Requirements</span></span>



| <span data-ttu-id="31781-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="31781-125">Requirement</span></span> | <span data-ttu-id="31781-126">Value</span><span class="sxs-lookup"><span data-stu-id="31781-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31781-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31781-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31781-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="31781-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31781-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31781-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31781-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="31781-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31781-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="31781-131">End of client support</span></span><br/>    | <span data-ttu-id="31781-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="31781-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="31781-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="31781-133">End of server support</span></span><br/>    | <span data-ttu-id="31781-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="31781-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="31781-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31781-135">Namespace</span></span><br/>                | <span data-ttu-id="31781-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="31781-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31781-137">MOF</span><span class="sxs-lookup"><span data-stu-id="31781-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31781-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31781-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31781-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31781-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31781-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31781-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="31781-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="31781-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31781-142">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="31781-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="31781-143">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="31781-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

