---
description: Destruye una instantánea existente de la colección de sistemas virtuales. Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Método DestroySnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666838"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="2cf5f-104">Método DestroySnapshot de la \_ clase CollectionSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="2cf5f-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="2cf5f-105">Destruye una instantánea existente de la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="2cf5f-106">Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf5f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cf5f-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2cf5f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cf5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf5f-109">*AffectedSnapshotCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2cf5f-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf5f-110">Referencia a una [**\_ colección CIM**](cim-collection.md) que describe la colección de instantáneas de sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="2cf5f-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2cf5f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf5f-112">Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="2cf5f-113">Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf5f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cf5f-114">Return value</span></span>

<span data-ttu-id="2cf5f-115">Si se ejecuta correctamente, devuelve 0 (completado) o 4096 (trabajo iniciado); de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2cf5f-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-122">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2cf5f-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="2cf5f-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2cf5f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf5f-127">Requirements</span></span>



| <span data-ttu-id="2cf5f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf5f-128">Requirement</span></span> | <span data-ttu-id="2cf5f-129">Value</span><span class="sxs-lookup"><span data-stu-id="2cf5f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf5f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf5f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf5f-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cf5f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2cf5f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf5f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf5f-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2cf5f-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2cf5f-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2cf5f-134">Namespace</span></span><br/>                | <span data-ttu-id="2cf5f-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2cf5f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2cf5f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2cf5f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cf5f-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cf5f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cf5f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cf5f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf5f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2cf5f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2cf5f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf5f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf5f-141">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="2cf5f-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




