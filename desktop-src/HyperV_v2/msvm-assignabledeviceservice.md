---
description: Administra los dispositivos asignables en un sistema de equipo host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688727"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="808f1-103">MSVM \_ AssignableDeviceService (clase)</span><span class="sxs-lookup"><span data-stu-id="808f1-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="808f1-104">Administra los dispositivos asignables en un sistema de equipo host.</span><span class="sxs-lookup"><span data-stu-id="808f1-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="808f1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="808f1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="808f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="808f1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="808f1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="808f1-107">Members</span></span>

<span data-ttu-id="808f1-108">La clase **MSVM \_ AssignableDeviceService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="808f1-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="808f1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="808f1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="808f1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="808f1-110">Methods</span></span>

<span data-ttu-id="808f1-111">La clase **MSVM \_ AssignableDeviceService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="808f1-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="808f1-112">Método</span><span class="sxs-lookup"><span data-stu-id="808f1-112">Method</span></span>                                                                                    | <span data-ttu-id="808f1-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="808f1-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="808f1-114">**DismountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="808f1-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="808f1-115">Desmonta el dispositivo PCI especificado para que se pueda asignar.</span><span class="sxs-lookup"><span data-stu-id="808f1-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="808f1-116">**MountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="808f1-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="808f1-117">Monta el dispositivo PCI especificado para que lo pueda usar el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="808f1-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="808f1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="808f1-118">Requirements</span></span>



| <span data-ttu-id="808f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="808f1-119">Requirement</span></span> | <span data-ttu-id="808f1-120">Value</span><span class="sxs-lookup"><span data-stu-id="808f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="808f1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="808f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="808f1-122">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="808f1-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="808f1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="808f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="808f1-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="808f1-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="808f1-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="808f1-125">Namespace</span></span><br/>                | <span data-ttu-id="808f1-126">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="808f1-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="808f1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="808f1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="808f1-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="808f1-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="808f1-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="808f1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="808f1-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="808f1-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="808f1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="808f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808f1-132">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="808f1-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




