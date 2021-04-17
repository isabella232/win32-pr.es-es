---
description: Servicio para crear, destruir y exportar la colección de instantáneas de sistemas virtuales.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666837"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="fa90e-103">MSVM \_ CollectionSnapshotService (clase)</span><span class="sxs-lookup"><span data-stu-id="fa90e-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="fa90e-104">Servicio para crear, destruir y exportar la colección de instantáneas de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fa90e-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="fa90e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fa90e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa90e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa90e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="fa90e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa90e-107">Members</span></span>

<span data-ttu-id="fa90e-108">La clase **MSVM \_ CollectionSnapshotService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fa90e-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="fa90e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa90e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa90e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa90e-110">Methods</span></span>

<span data-ttu-id="fa90e-111">La clase **MSVM \_ CollectionSnapshotService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fa90e-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="fa90e-112">Método</span><span class="sxs-lookup"><span data-stu-id="fa90e-112">Method</span></span>                                                                                    | <span data-ttu-id="fa90e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa90e-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa90e-114">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="fa90e-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="fa90e-115">Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="fa90e-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="fa90e-116">**ConvertToReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="fa90e-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="fa90e-117">Convertir una instantánea de colección existente en una colección de puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="fa90e-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="fa90e-118">La colección de instantáneas se elimina como un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="fa90e-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="fa90e-119">Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="fa90e-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="fa90e-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="fa90e-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="fa90e-121">Crea una instantánea de una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fa90e-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="fa90e-122">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="fa90e-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="fa90e-123">Destruya una instantánea existente de la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fa90e-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="fa90e-124">Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.</span><span class="sxs-lookup"><span data-stu-id="fa90e-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="fa90e-125">**ExportSnapshot**</span><span class="sxs-lookup"><span data-stu-id="fa90e-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="fa90e-126">Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo.</span><span class="sxs-lookup"><span data-stu-id="fa90e-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="fa90e-127">La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.</span><span class="sxs-lookup"><span data-stu-id="fa90e-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa90e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa90e-128">Requirements</span></span>



| <span data-ttu-id="fa90e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa90e-129">Requirement</span></span> | <span data-ttu-id="fa90e-130">Value</span><span class="sxs-lookup"><span data-stu-id="fa90e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa90e-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa90e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fa90e-132">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa90e-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fa90e-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa90e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fa90e-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fa90e-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fa90e-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa90e-135">Namespace</span></span><br/>                | <span data-ttu-id="fa90e-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fa90e-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fa90e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fa90e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa90e-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa90e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa90e-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa90e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa90e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa90e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa90e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa90e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa90e-142">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="fa90e-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




