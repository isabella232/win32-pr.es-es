---
description: Recupera un error.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Método GetError de la clase Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083268"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="bd66e-103">Método GetError de la \_ clase CollectionReferencePointExportJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="bd66e-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="bd66e-104">Recupera un error.</span><span class="sxs-lookup"><span data-stu-id="bd66e-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd66e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd66e-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="bd66e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd66e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd66e-107">*Error* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bd66e-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd66e-108">Si se ejecuta correctamente, contiene una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="bd66e-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd66e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd66e-109">Return value</span></span>

<span data-ttu-id="bd66e-110">0 si se ejecuta correctamente; de lo contrario, un error.</span><span class="sxs-lookup"><span data-stu-id="bd66e-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="bd66e-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bd66e-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="bd66e-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bd66e-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="bd66e-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-115">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bd66e-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-116">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="bd66e-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-117">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bd66e-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-118">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bd66e-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-119">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="bd66e-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-120">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bd66e-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-121">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bd66e-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bd66e-122">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bd66e-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bd66e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd66e-123">Requirements</span></span>



| <span data-ttu-id="bd66e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd66e-124">Requirement</span></span> | <span data-ttu-id="bd66e-125">Value</span><span class="sxs-lookup"><span data-stu-id="bd66e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd66e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd66e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bd66e-127">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd66e-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd66e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd66e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bd66e-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bd66e-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bd66e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd66e-130">Namespace</span></span><br/>                | <span data-ttu-id="bd66e-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bd66e-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bd66e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bd66e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd66e-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd66e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd66e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd66e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd66e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd66e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd66e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd66e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd66e-137">**MSVM \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="bd66e-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




