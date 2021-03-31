---
description: Destruye una colección de puntos de referencia existente. Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Método DestroyReferencePoint de la clase Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156861"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="b968c-104">Método DestroyReferencePoint de la \_ clase CollectionReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b968c-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="b968c-105">Destruye una colección de puntos de referencia existente.</span><span class="sxs-lookup"><span data-stu-id="b968c-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="b968c-106">Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.</span><span class="sxs-lookup"><span data-stu-id="b968c-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b968c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b968c-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b968c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b968c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b968c-109">*AffectedReferencePointCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b968c-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b968c-110">Referencia a la colección de puntos de referencia del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="b968c-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="b968c-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b968c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b968c-112">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="b968c-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b968c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b968c-113">Return value</span></span>

<span data-ttu-id="b968c-114">Si se realiza correctamente, devuelve 0 (sin errores) o 4096 (se inició el trabajo). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="b968c-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="b968c-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b968c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b968c-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-117">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="b968c-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="b968c-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-119">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="b968c-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-120">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="b968c-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-121">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="b968c-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b968c-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b968c-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b968c-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b968c-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="b968c-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b968c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b968c-126">Requirements</span></span>



| <span data-ttu-id="b968c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b968c-127">Requirement</span></span> | <span data-ttu-id="b968c-128">Value</span><span class="sxs-lookup"><span data-stu-id="b968c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b968c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b968c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b968c-130">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b968c-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b968c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b968c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b968c-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b968c-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b968c-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b968c-133">Namespace</span></span><br/>                | <span data-ttu-id="b968c-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b968c-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b968c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b968c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b968c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b968c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b968c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b968c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b968c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b968c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b968c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b968c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b968c-140">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="b968c-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




