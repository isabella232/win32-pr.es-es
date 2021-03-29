---
description: Destruya una instantánea del sistema virtual existente. Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Método DestroySnapshot de la clase CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542390"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="4f46e-104">Método DestroySnapshot de la \_ clase VirtualSystemSnapshotService de CIM</span><span class="sxs-lookup"><span data-stu-id="4f46e-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="4f46e-105">Destruya una instantánea del sistema virtual existente.</span><span class="sxs-lookup"><span data-stu-id="4f46e-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="4f46e-106">Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.</span><span class="sxs-lookup"><span data-stu-id="4f46e-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f46e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f46e-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4f46e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f46e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f46e-109">*AffectedSnapshot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f46e-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f46e-110">Una [**referencia \_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) a la instantánea del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="4f46e-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4f46e-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4f46e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f46e-112">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="4f46e-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="4f46e-113">Este parámetro era de lectura/escritura en Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4f46e-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f46e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f46e-114">Return value</span></span>

<span data-ttu-id="4f46e-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4f46e-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4f46e-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="4f46e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="4f46e-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="4f46e-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="4f46e-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="4f46e-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="4f46e-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-122">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="4f46e-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4f46e-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4f46e-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4f46e-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4f46e-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="4f46e-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4f46e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f46e-127">Requirements</span></span>



| <span data-ttu-id="4f46e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f46e-128">Requirement</span></span> | <span data-ttu-id="4f46e-129">Value</span><span class="sxs-lookup"><span data-stu-id="4f46e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f46e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f46e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4f46e-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4f46e-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4f46e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f46e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4f46e-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4f46e-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4f46e-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f46e-134">Namespace</span></span><br/>                | <span data-ttu-id="4f46e-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4f46e-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4f46e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4f46e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f46e-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f46e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f46e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f46e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f46e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f46e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f46e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f46e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f46e-141">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4f46e-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




