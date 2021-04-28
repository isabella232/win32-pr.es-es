---
description: 'Método RemoveAssociatedData de la clase Msvm_CollectionReferencePointService : quita el registro de datos asociado al punto de referencia.'
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Método RemoveAssociatedData de la Msvm_CollectionReferencePointService clase
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
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119233"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="2154a-103">Método RemoveAssociatedData de la clase CollectionReferencePointService de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="2154a-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="2154a-104">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="2154a-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="2154a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2154a-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2154a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2154a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2154a-107">*AffectedReferencePointCollection* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2154a-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154a-108">Referencia a la colección de puntos de referencia del sistema virtual afectado.</span><span class="sxs-lookup"><span data-stu-id="2154a-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="2154a-109">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2154a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2154a-110">Si la operación es de larga duración, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="2154a-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2154a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2154a-111">Return value</span></span>

<span data-ttu-id="2154a-112">Si se realiza correctamente, devuelve 0 (sin error) o 4096 (trabajo iniciado); de lo contrario, devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="2154a-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="2154a-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2154a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2154a-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="2154a-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-116">**Tiempo de** espera (3)</span><span class="sxs-lookup"><span data-stu-id="2154a-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="2154a-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="2154a-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-119">**Tipo no** válido (6)</span><span class="sxs-lookup"><span data-stu-id="2154a-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2154a-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2154a-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-122">**Método reservado** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="2154a-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2154a-123">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2154a-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2154a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2154a-124">Requirements</span></span>



| <span data-ttu-id="2154a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2154a-125">Requirement</span></span> | <span data-ttu-id="2154a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2154a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2154a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2154a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2154a-128">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="2154a-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2154a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2154a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2154a-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2154a-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2154a-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2154a-131">Namespace</span></span><br/>                | <span data-ttu-id="2154a-132">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="2154a-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2154a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2154a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2154a-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2154a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2154a-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2154a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2154a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2154a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2154a-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2154a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2154a-138">**Colección de \_ MsvmReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="2154a-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




