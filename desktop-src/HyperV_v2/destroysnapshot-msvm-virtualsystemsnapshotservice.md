---
description: Destruye una instantánea de máquina virtual existente.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Método DestroySnapshot de la clase Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912849"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="3fb9f-103">Método DestroySnapshot de la \_ clase VirtualSystemSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="3fb9f-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="3fb9f-104">Destruye una instantánea de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="3fb9f-105">Este método puede, como efecto secundario, destruir otras instantáneas que dependen de la instantánea afectada.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb9f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb9f-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3fb9f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fb9f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb9f-108">*AffectedSnapshot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fb9f-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb9f-109">Referencia [**de \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea de la máquina virtual que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="3fb9f-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3fb9f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb9f-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3fb9f-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb9f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fb9f-112">Return value</span></span>

<span data-ttu-id="3fb9f-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3fb9f-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-120">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3fb9f-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3fb9f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb9f-125">Requirements</span></span>



| <span data-ttu-id="3fb9f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb9f-126">Requirement</span></span> | <span data-ttu-id="3fb9f-127">Value</span><span class="sxs-lookup"><span data-stu-id="3fb9f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb9f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb9f-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fb9f-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fb9f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb9f-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fb9f-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fb9f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fb9f-132">Namespace</span></span><br/>                | <span data-ttu-id="3fb9f-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fb9f-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fb9f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb9f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb9f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fb9f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb9f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fb9f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb9f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fb9f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fb9f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fb9f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb9f-139">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="3fb9f-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="3fb9f-140">**RemoveVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="3fb9f-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

