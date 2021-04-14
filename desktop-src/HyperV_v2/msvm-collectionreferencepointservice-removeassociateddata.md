---
description: Quita el registro de datos asociado al punto de referencia.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Método RemoveAssociatedData de la clase Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aec1ac249616c08c6abf1f156ad5a3416c8afaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668426"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="fff99-103">Método RemoveAssociatedData de la \_ clase CollectionReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="fff99-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="fff99-104">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="fff99-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fff99-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fff99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fff99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff99-107">*AffectedReferencePointCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fff99-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff99-108">Referencia a la colección de puntos de referencia del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="fff99-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="fff99-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fff99-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fff99-110">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="fff99-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff99-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fff99-111">Return value</span></span>

<span data-ttu-id="fff99-112">Si se realiza correctamente, devuelve 0 (sin errores) o 4096 (se inició el trabajo). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="fff99-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="fff99-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="fff99-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="fff99-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="fff99-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="fff99-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="fff99-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="fff99-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-119">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="fff99-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fff99-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fff99-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fff99-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fff99-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="fff99-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fff99-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fff99-124">Requirements</span></span>



| <span data-ttu-id="fff99-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff99-125">Requirement</span></span> | <span data-ttu-id="fff99-126">Value</span><span class="sxs-lookup"><span data-stu-id="fff99-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff99-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fff99-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fff99-128">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fff99-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fff99-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fff99-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fff99-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fff99-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fff99-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fff99-131">Namespace</span></span><br/>                | <span data-ttu-id="fff99-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fff99-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fff99-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fff99-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff99-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff99-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff99-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fff99-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff99-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fff99-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fff99-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fff99-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff99-138">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="fff99-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




