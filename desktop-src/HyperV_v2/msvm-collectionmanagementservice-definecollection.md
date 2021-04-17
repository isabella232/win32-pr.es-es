---
description: Crea un nuevo \_ objeto CIM CollectionOfMSEs.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Método DefineCollection de la clase Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688370"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="ef620-103">Método DefineCollection de la \_ clase CollectionManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ef620-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="ef620-104">Crea un nuevo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="ef620-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef620-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef620-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ef620-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef620-107">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ef620-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef620-108">Nombre de la nueva colección.</span><span class="sxs-lookup"><span data-stu-id="ef620-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="ef620-109">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ef620-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef620-110">IDENTIFICADOR de la nueva colección.</span><span class="sxs-lookup"><span data-stu-id="ef620-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="ef620-111">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ef620-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef620-112">Tipo de la nueva colección.</span><span class="sxs-lookup"><span data-stu-id="ef620-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="ef620-113">**Colección de sistemas virtuales** (0)</span><span class="sxs-lookup"><span data-stu-id="ef620-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="ef620-114">**Colección de colecciones** (1)</span><span class="sxs-lookup"><span data-stu-id="ef620-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ef620-115">*DefinedCollection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ef620-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef620-116">Referencia a los objetos que definen la colección.</span><span class="sxs-lookup"><span data-stu-id="ef620-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ef620-117">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ef620-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef620-118">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="ef620-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef620-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef620-119">Return value</span></span>

<span data-ttu-id="ef620-120">Si se realiza correctamente, devuelve 0 o 4096 (se inició el trabajo); de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ef620-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ef620-121">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ef620-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ef620-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-123">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ef620-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-124">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ef620-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-125">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ef620-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-126">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ef620-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-127">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ef620-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-128">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ef620-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-129">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ef620-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-130">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ef620-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-131">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ef620-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-132">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ef620-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-133">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ef620-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ef620-134">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="ef620-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ef620-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef620-135">Requirements</span></span>



| <span data-ttu-id="ef620-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef620-136">Requirement</span></span> | <span data-ttu-id="ef620-137">Value</span><span class="sxs-lookup"><span data-stu-id="ef620-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef620-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef620-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ef620-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef620-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ef620-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef620-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ef620-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ef620-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ef620-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef620-142">Namespace</span></span><br/>                | <span data-ttu-id="ef620-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ef620-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef620-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ef620-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef620-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef620-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef620-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef620-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef620-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef620-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef620-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef620-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef620-149">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="ef620-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




