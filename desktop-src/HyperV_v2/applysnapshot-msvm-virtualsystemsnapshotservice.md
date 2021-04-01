---
description: Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Método ApplySnapshot de la clase Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909841"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="94e94-103">Método ApplySnapshot de la \_ clase VirtualSystemSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="94e94-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="94e94-104">Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.</span><span class="sxs-lookup"><span data-stu-id="94e94-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94e94-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="94e94-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94e94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e94-107">*Instantánea* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="94e94-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94e94-108">Referencia a una clase derivada de [**\_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea de la máquina virtual que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="94e94-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="94e94-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="94e94-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94e94-110">Esta operación siempre se realiza de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="94e94-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="94e94-111">Este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob de CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e94-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94e94-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94e94-112">Return value</span></span>

<span data-ttu-id="94e94-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="94e94-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="94e94-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="94e94-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="94e94-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="94e94-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="94e94-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="94e94-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="94e94-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-120">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="94e94-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="94e94-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="94e94-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-123">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="94e94-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="94e94-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-125">**Estado no válido** (32775)</span><span class="sxs-lookup"><span data-stu-id="94e94-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-126">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="94e94-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="94e94-127">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="94e94-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="94e94-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e94-128">Requirements</span></span>



| <span data-ttu-id="94e94-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e94-129">Requirement</span></span> | <span data-ttu-id="94e94-130">Value</span><span class="sxs-lookup"><span data-stu-id="94e94-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e94-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e94-131">Minimum supported client</span></span><br/> | <span data-ttu-id="94e94-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="94e94-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94e94-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e94-133">Minimum supported server</span></span><br/> | <span data-ttu-id="94e94-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="94e94-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94e94-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94e94-135">Namespace</span></span><br/>                | <span data-ttu-id="94e94-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="94e94-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94e94-137">MOF</span><span class="sxs-lookup"><span data-stu-id="94e94-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94e94-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94e94-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94e94-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94e94-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94e94-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94e94-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94e94-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="94e94-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e94-142">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="94e94-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="94e94-143">**ApplyVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="94e94-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="94e94-144">**ApplyVirtualSystemSnapshotEx (V1)**</span><span class="sxs-lookup"><span data-stu-id="94e94-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

