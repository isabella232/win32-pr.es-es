---
description: Aplica una instantánea del sistema virtual al sistema virtual desde el que se creó.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Método ApplySnapshot de la clase CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688076"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="47c3f-103">Método ApplySnapshot de la \_ clase VirtualSystemSnapshotService de CIM</span><span class="sxs-lookup"><span data-stu-id="47c3f-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="47c3f-104">Aplica una instantánea del sistema virtual al sistema virtual desde el que se creó.</span><span class="sxs-lookup"><span data-stu-id="47c3f-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47c3f-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="47c3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47c3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c3f-107">*Instantánea* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="47c3f-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3f-108">Una [**referencia \_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) a la instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="47c3f-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="47c3f-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="47c3f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3f-110">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="47c3f-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="47c3f-111">Este parámetro era de lectura/escritura en Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="47c3f-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c3f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47c3f-112">Return value</span></span>

<span data-ttu-id="47c3f-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="47c3f-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="47c3f-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="47c3f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="47c3f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="47c3f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="47c3f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="47c3f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="47c3f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-120">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="47c3f-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="47c3f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="47c3f-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="47c3f-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="47c3f-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="47c3f-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="47c3f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c3f-125">Requirements</span></span>



| <span data-ttu-id="47c3f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c3f-126">Requirement</span></span> | <span data-ttu-id="47c3f-127">Value</span><span class="sxs-lookup"><span data-stu-id="47c3f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c3f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="47c3f-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="47c3f-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="47c3f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="47c3f-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="47c3f-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="47c3f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47c3f-132">Namespace</span></span><br/>                | <span data-ttu-id="47c3f-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="47c3f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="47c3f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="47c3f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c3f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c3f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c3f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47c3f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c3f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47c3f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47c3f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="47c3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c3f-139">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="47c3f-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




