---
description: Representa un servicio que administra los sistemas virtuales.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667089"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="60896-103">\_Clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="60896-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="60896-104">Representa un servicio que administra los sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="60896-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="60896-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60896-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="60896-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="60896-106">Members</span></span>

<span data-ttu-id="60896-107">La clase **CIM \_ VirtualSystemManagementService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60896-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="60896-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="60896-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60896-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="60896-109">Methods</span></span>

<span data-ttu-id="60896-110">La clase **CIM \_ VirtualSystemManagementService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="60896-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="60896-111">Método</span><span class="sxs-lookup"><span data-stu-id="60896-111">Method</span></span>                                                                                      | <span data-ttu-id="60896-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60896-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="60896-113">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="60896-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="60896-114">Agrega recursos a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="60896-115">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="60896-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="60896-116">Define un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="60896-117">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="60896-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="60896-118">Elimina un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="60896-119">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="60896-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="60896-120">Modifica la configuración de recursos virtuales para una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="60896-121">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="60896-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="60896-122">Modifica la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="60896-123">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="60896-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="60896-124">Quita la configuración de recursos virtuales de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60896-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="60896-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60896-125">Requirements</span></span>



| <span data-ttu-id="60896-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="60896-126">Requirement</span></span> | <span data-ttu-id="60896-127">Value</span><span class="sxs-lookup"><span data-stu-id="60896-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60896-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60896-128">Minimum supported client</span></span><br/> | <span data-ttu-id="60896-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60896-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="60896-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60896-130">Minimum supported server</span></span><br/> | <span data-ttu-id="60896-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60896-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="60896-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60896-132">Namespace</span></span><br/>                | <span data-ttu-id="60896-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="60896-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60896-134">MOF</span><span class="sxs-lookup"><span data-stu-id="60896-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60896-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60896-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60896-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60896-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60896-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60896-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60896-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="60896-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60896-139">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="60896-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




