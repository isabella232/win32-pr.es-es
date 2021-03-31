---
description: Recupera el error.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Método GetError de la clase Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083546"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="26c73-103">Método GetError de la \_ clase VirtualSystemReferencePointExportJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="26c73-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="26c73-104">Recupera el error.</span><span class="sxs-lookup"><span data-stu-id="26c73-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26c73-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="26c73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26c73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c73-107">*Error* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="26c73-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26c73-108">Error recuperado.</span><span class="sxs-lookup"><span data-stu-id="26c73-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c73-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26c73-109">Return value</span></span>

<span data-ttu-id="26c73-110">Si se ejecuta correctamente, devuelve un 0; de lo contrario, contiene un error.</span><span class="sxs-lookup"><span data-stu-id="26c73-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="26c73-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="26c73-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="26c73-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="26c73-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="26c73-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-115">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="26c73-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-116">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="26c73-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-117">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="26c73-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-118">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="26c73-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-119">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="26c73-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-120">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="26c73-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-121">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="26c73-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="26c73-122">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="26c73-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="26c73-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26c73-123">Requirements</span></span>



| <span data-ttu-id="26c73-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c73-124">Requirement</span></span> | <span data-ttu-id="26c73-125">Value</span><span class="sxs-lookup"><span data-stu-id="26c73-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c73-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26c73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26c73-127">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="26c73-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="26c73-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26c73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26c73-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="26c73-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="26c73-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26c73-130">Namespace</span></span><br/>                | <span data-ttu-id="26c73-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="26c73-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26c73-132">MOF</span><span class="sxs-lookup"><span data-stu-id="26c73-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26c73-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26c73-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26c73-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26c73-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c73-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26c73-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26c73-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="26c73-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c73-137">**MSVM \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="26c73-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




