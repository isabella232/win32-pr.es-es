---
description: Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Método ApplySnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686743"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="410ab-103">Método ApplySnapshot de la \_ clase CollectionSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="410ab-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="410ab-104">Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="410ab-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="410ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="410ab-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="410ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="410ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="410ab-107">*SnapshotCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="410ab-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410ab-108">Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de instantáneas que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="410ab-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="410ab-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="410ab-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="410ab-110">Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="410ab-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="410ab-111">Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="410ab-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="410ab-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="410ab-112">Return value</span></span>

<span data-ttu-id="410ab-113">Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="410ab-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="410ab-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="410ab-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="410ab-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="410ab-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="410ab-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="410ab-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="410ab-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-120">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="410ab-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="410ab-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="410ab-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="410ab-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="410ab-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="410ab-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="410ab-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="410ab-125">Requirements</span></span>



| <span data-ttu-id="410ab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="410ab-126">Requirement</span></span> | <span data-ttu-id="410ab-127">Value</span><span class="sxs-lookup"><span data-stu-id="410ab-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410ab-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="410ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="410ab-129">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="410ab-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="410ab-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="410ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="410ab-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="410ab-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="410ab-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="410ab-132">Namespace</span></span><br/>                | <span data-ttu-id="410ab-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="410ab-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="410ab-134">MOF</span><span class="sxs-lookup"><span data-stu-id="410ab-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="410ab-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="410ab-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="410ab-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="410ab-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="410ab-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="410ab-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="410ab-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="410ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410ab-139">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="410ab-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




