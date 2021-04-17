---
description: Quita una instantánea existente, y todos sus elementos secundarios, de una máquina virtual.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Método DestroySnapshotTree de la clase Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668086"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="9ffb3-103">Método DestroySnapshotTree de la \_ clase VirtualSystemSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9ffb3-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="9ffb3-104">Quita una instantánea existente, y todos sus elementos secundarios, de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9ffb3-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffb3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ffb3-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9ffb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ffb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ffb3-107">*SnapshotSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ffb3-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffb3-108">Referencia [**de \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa el árbol de instantáneas de la máquina virtual que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="9ffb3-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="9ffb3-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ffb3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffb3-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ffb3-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ffb3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ffb3-111">Return value</span></span>

<span data-ttu-id="9ffb3-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ffb3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9ffb3-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9ffb3-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9ffb3-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9ffb3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ffb3-126">Requirements</span></span>



| <span data-ttu-id="9ffb3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffb3-127">Requirement</span></span> | <span data-ttu-id="9ffb3-128">Value</span><span class="sxs-lookup"><span data-stu-id="9ffb3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffb3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ffb3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffb3-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ffb3-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9ffb3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ffb3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffb3-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ffb3-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ffb3-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ffb3-133">Namespace</span></span><br/>                | <span data-ttu-id="9ffb3-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9ffb3-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9ffb3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9ffb3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ffb3-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ffb3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ffb3-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ffb3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ffb3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ffb3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9ffb3-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ffb3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffb3-140">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="9ffb3-141">**RemoveVirtualSystemSnapshotTree (V1)**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

