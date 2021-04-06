---
description: Representa el servicio de seguridad. Se usa para configurar las opciones de seguridad del sistema virtual.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002091"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="646dd-104">MSVM \_ SecurityService (clase)</span><span class="sxs-lookup"><span data-stu-id="646dd-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="646dd-105">Representa el servicio de seguridad.</span><span class="sxs-lookup"><span data-stu-id="646dd-105">Represents the security service.</span></span> <span data-ttu-id="646dd-106">Se usa para configurar las opciones de seguridad del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="646dd-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="646dd-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="646dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="646dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="646dd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="646dd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="646dd-109">Members</span></span>

<span data-ttu-id="646dd-110">La clase **MSVM \_ SecurityService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="646dd-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="646dd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="646dd-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="646dd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="646dd-112">Methods</span></span>

<span data-ttu-id="646dd-113">La clase **MSVM \_ SecurityService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="646dd-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="646dd-114">Método</span><span class="sxs-lookup"><span data-stu-id="646dd-114">Method</span></span>                                                                                            | <span data-ttu-id="646dd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="646dd-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="646dd-116">**GetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="646dd-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="646dd-117">Método para recuperar el protector de clave de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="646dd-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="646dd-118">**ModifySecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="646dd-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="646dd-119">Modifica la configuración de seguridad actual de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="646dd-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="646dd-120">**RestoreLastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="646dd-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="646dd-121">Método que se va a restaurar al último protector de clave válido conocido.</span><span class="sxs-lookup"><span data-stu-id="646dd-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="646dd-122">**SetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="646dd-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="646dd-123">Método para establecer el protector de clave de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="646dd-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="646dd-124">**SetSecurityPolicy**</span><span class="sxs-lookup"><span data-stu-id="646dd-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="646dd-125">Método para establecer el protector de clave de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="646dd-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="646dd-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="646dd-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="646dd-127">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="646dd-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="646dd-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="646dd-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="646dd-129">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="646dd-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="646dd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="646dd-130">Requirements</span></span>



| <span data-ttu-id="646dd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="646dd-131">Requirement</span></span> | <span data-ttu-id="646dd-132">Value</span><span class="sxs-lookup"><span data-stu-id="646dd-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="646dd-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="646dd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="646dd-134">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="646dd-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="646dd-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="646dd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="646dd-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="646dd-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="646dd-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="646dd-137">Namespace</span></span><br/>                | <span data-ttu-id="646dd-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="646dd-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="646dd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="646dd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="646dd-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="646dd-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="646dd-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="646dd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="646dd-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="646dd-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="646dd-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="646dd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646dd-144">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="646dd-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




