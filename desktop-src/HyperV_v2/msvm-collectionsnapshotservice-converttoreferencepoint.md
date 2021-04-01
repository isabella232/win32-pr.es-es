---
description: Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Método ConvertToReferencePoint de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913702"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="28906-105">Método ConvertToReferencePoint de la \_ clase CollectionSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="28906-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="28906-106">Convertir una instantánea de colección existente en una colección de puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="28906-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="28906-107">La colección de instantáneas se elimina como un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="28906-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="28906-108">Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="28906-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="28906-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28906-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28906-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28906-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28906-111">*AffectedSnapshotCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28906-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28906-112">Referencia a un [**\_ SnapshotCollection de MSVM**](msvm-snapshotcollection.md) que contiene la colección de instantáneas del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="28906-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="28906-113">*ResultingReferencePointCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28906-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28906-114">Referencia a un [**\_ ReferencePointCollection de MSVM**](msvm-referencepointcollection.md) que contiene la colección de puntos de referencia del sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="28906-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="28906-115">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28906-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28906-116">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="28906-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28906-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28906-117">Return value</span></span>

<span data-ttu-id="28906-118">Si se ejecuta correctamente, devuelve 0 (completado) o 4096 (trabajo iniciado); de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="28906-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="28906-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="28906-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28906-120">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="28906-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="28906-121">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="28906-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="28906-122">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="28906-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="28906-123">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="28906-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="28906-124">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="28906-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="28906-125">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="28906-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="28906-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="28906-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="28906-127">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="28906-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28906-128">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="28906-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="28906-129">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="28906-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="28906-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28906-130">Requirements</span></span>



| <span data-ttu-id="28906-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="28906-131">Requirement</span></span> | <span data-ttu-id="28906-132">Value</span><span class="sxs-lookup"><span data-stu-id="28906-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28906-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28906-133">Minimum supported client</span></span><br/> | <span data-ttu-id="28906-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="28906-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="28906-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28906-135">Minimum supported server</span></span><br/> | <span data-ttu-id="28906-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="28906-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="28906-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28906-137">Namespace</span></span><br/>                | <span data-ttu-id="28906-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="28906-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="28906-139">MOF</span><span class="sxs-lookup"><span data-stu-id="28906-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28906-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28906-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28906-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28906-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28906-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28906-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28906-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="28906-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28906-144">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="28906-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




