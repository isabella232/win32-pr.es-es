---
description: Administra las capacidades de la instancia de ResourcePoolConfigurationService de CIM \_ para un \_ objeto RESOURCEPOOL de CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: CIM_ResourcePoolConfigurationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686910"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="7df61-103">\_Clase ResourcePoolConfigurationCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="7df61-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="7df61-104">Administra las capacidades de la instancia de [**\_ ResourcePoolConfigurationService de CIM**](cim-resourcepoolconfigurationservice.md) para un objeto [**\_ ResourcePool de CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="7df61-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7df61-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="7df61-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7df61-106">Members</span></span>

<span data-ttu-id="7df61-107">La clase **CIM \_ ResourcePoolConfigurationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7df61-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="7df61-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7df61-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7df61-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7df61-109">Properties</span></span>

<span data-ttu-id="7df61-110">La clase **CIM \_ ResourcePoolConfigurationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7df61-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7df61-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="7df61-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7df61-112">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="7df61-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="7df61-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7df61-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7df61-114">Los métodos del servicio de configuración que se admiten para las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="7df61-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-115">**Se admite CreateResourcePool** (2)</span><span class="sxs-lookup"><span data-stu-id="7df61-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-116">**Se admite CreateChild ResourcePool** (3)</span><span class="sxs-lookup"><span data-stu-id="7df61-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-117">**Se admite DeleteResourcePool** (4)</span><span class="sxs-lookup"><span data-stu-id="7df61-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-118">**Se admite AddResourcesToResourcePool** (5)</span><span class="sxs-lookup"><span data-stu-id="7df61-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-119">**Se admite RemoveResourcesFromResourcePool** (6)</span><span class="sxs-lookup"><span data-stu-id="7df61-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-120">**Se admite ChangeParentResourcePool** (7)</span><span class="sxs-lookup"><span data-stu-id="7df61-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7df61-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7df61-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7df61-122">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7df61-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7df61-123">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="7df61-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7df61-124">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="7df61-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="7df61-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7df61-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7df61-126">Los métodos del servicio de configuración que se admiten para las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="7df61-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-127">**Se admite CreateResourcePool** (2)</span><span class="sxs-lookup"><span data-stu-id="7df61-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-128">**Se admite CreateChild ResourcePool** (3)</span><span class="sxs-lookup"><span data-stu-id="7df61-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-129">**Se admite DeleteResourcePool** (4)</span><span class="sxs-lookup"><span data-stu-id="7df61-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-130">**Se admite AddResourcesToResourcePool** (5)</span><span class="sxs-lookup"><span data-stu-id="7df61-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-131">**Se admite RemoveResourcesFromResourcePool** (6)</span><span class="sxs-lookup"><span data-stu-id="7df61-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="7df61-132">**CIM \_ Se admite ChangeParentResourcePool** (7)</span><span class="sxs-lookup"><span data-stu-id="7df61-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7df61-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7df61-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7df61-134">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7df61-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="7df61-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7df61-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7df61-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df61-136">Requirements</span></span>



| <span data-ttu-id="7df61-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df61-137">Requirement</span></span> | <span data-ttu-id="7df61-138">Value</span><span class="sxs-lookup"><span data-stu-id="7df61-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df61-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df61-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7df61-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7df61-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7df61-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df61-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7df61-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7df61-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7df61-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7df61-143">Namespace</span></span><br/>                | <span data-ttu-id="7df61-144">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7df61-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7df61-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7df61-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7df61-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7df61-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7df61-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7df61-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df61-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7df61-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7df61-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df61-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df61-150">**Capacidades de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7df61-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




