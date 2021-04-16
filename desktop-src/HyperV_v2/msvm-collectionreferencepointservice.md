---
description: Servicio para crear, destruir y exportar puntos de referencia.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687029"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="6684f-103">MSVM \_ CollectionReferencePointService (clase)</span><span class="sxs-lookup"><span data-stu-id="6684f-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="6684f-104">Servicio para crear, destruir y exportar puntos de referencia</span><span class="sxs-lookup"><span data-stu-id="6684f-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="6684f-105">de colecciones del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6684f-105">of virtual system collections.</span></span>

<span data-ttu-id="6684f-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6684f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6684f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6684f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="6684f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6684f-108">Members</span></span>

<span data-ttu-id="6684f-109">La clase **MSVM \_ CollectionReferencePointService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6684f-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="6684f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6684f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6684f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6684f-111">Methods</span></span>

<span data-ttu-id="6684f-112">La clase **MSVM \_ CollectionReferencePointService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6684f-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="6684f-113">Método</span><span class="sxs-lookup"><span data-stu-id="6684f-113">Method</span></span>                                                                                      | <span data-ttu-id="6684f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6684f-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6684f-115">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="6684f-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="6684f-116">Crea un punto de referencia de una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="6684f-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="6684f-117">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="6684f-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="6684f-118">Destruye una colección de puntos de referencia existente.</span><span class="sxs-lookup"><span data-stu-id="6684f-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="6684f-119">Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.</span><span class="sxs-lookup"><span data-stu-id="6684f-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="6684f-120">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="6684f-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="6684f-121">Exporta una colección de puntos de referencia a un archivo.</span><span class="sxs-lookup"><span data-stu-id="6684f-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="6684f-122">La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.</span><span class="sxs-lookup"><span data-stu-id="6684f-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="6684f-123">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="6684f-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="6684f-124">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="6684f-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="6684f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6684f-125">Requirements</span></span>



| <span data-ttu-id="6684f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6684f-126">Requirement</span></span> | <span data-ttu-id="6684f-127">Value</span><span class="sxs-lookup"><span data-stu-id="6684f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6684f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6684f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6684f-129">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6684f-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6684f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6684f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6684f-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6684f-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6684f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6684f-132">Namespace</span></span><br/>                | <span data-ttu-id="6684f-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6684f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6684f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6684f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6684f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6684f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6684f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6684f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6684f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6684f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6684f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6684f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6684f-139">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="6684f-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




