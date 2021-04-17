---
description: Describe un servicio de punto de referencia del sistema virtual.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670063"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="2e52a-103">MSVM \_ VirtualSystemReferencePointService (clase)</span><span class="sxs-lookup"><span data-stu-id="2e52a-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="2e52a-104">Describe un servicio de punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2e52a-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="2e52a-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2e52a-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e52a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e52a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="2e52a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e52a-107">Members</span></span>

<span data-ttu-id="2e52a-108">La clase **MSVM \_ VirtualSystemReferencePointService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e52a-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="2e52a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e52a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e52a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e52a-110">Methods</span></span>

<span data-ttu-id="2e52a-111">La clase **MSVM \_ VirtualSystemReferencePointService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e52a-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="2e52a-112">Método</span><span class="sxs-lookup"><span data-stu-id="2e52a-112">Method</span></span>                                                                                                       | <span data-ttu-id="2e52a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e52a-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="2e52a-114">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="2e52a-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="2e52a-115">Crea un punto de referencia de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2e52a-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="2e52a-116">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="2e52a-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="2e52a-117">Elimina el punto de referencia especificado.</span><span class="sxs-lookup"><span data-stu-id="2e52a-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="2e52a-118">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="2e52a-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="2e52a-119">Exporta el punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2e52a-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="2e52a-120">**ImportReferencePointMetadata**</span><span class="sxs-lookup"><span data-stu-id="2e52a-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="2e52a-121">Importa los metadatos del punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2e52a-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="2e52a-122">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="2e52a-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="2e52a-123">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="2e52a-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e52a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e52a-124">Requirements</span></span>



| <span data-ttu-id="2e52a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e52a-125">Requirement</span></span> | <span data-ttu-id="2e52a-126">Value</span><span class="sxs-lookup"><span data-stu-id="2e52a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e52a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e52a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e52a-128">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e52a-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2e52a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e52a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e52a-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2e52a-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2e52a-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e52a-131">Namespace</span></span><br/>                | <span data-ttu-id="2e52a-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2e52a-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e52a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2e52a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e52a-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e52a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e52a-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e52a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e52a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e52a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e52a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e52a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e52a-138">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="2e52a-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




