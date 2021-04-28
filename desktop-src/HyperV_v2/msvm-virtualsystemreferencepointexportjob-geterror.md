---
description: 'Método GetError de la Msvm_VirtualSystemReferencePointExportJob : recupera el error.'
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Método GetError de la Msvm_VirtualSystemReferencePointExportJob clase
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
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109343"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="53eb8-103">Método GetError de la clase Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="53eb8-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="53eb8-104">Recupera el error.</span><span class="sxs-lookup"><span data-stu-id="53eb8-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="53eb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53eb8-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="53eb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53eb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53eb8-107">*Error* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53eb8-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53eb8-108">Error recuperado.</span><span class="sxs-lookup"><span data-stu-id="53eb8-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53eb8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53eb8-109">Return value</span></span>

<span data-ttu-id="53eb8-110">Si se ejecuta correctamente, devuelve 0; de lo contrario, contiene un error.</span><span class="sxs-lookup"><span data-stu-id="53eb8-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="53eb8-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="53eb8-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="53eb8-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="53eb8-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="53eb8-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-115">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="53eb8-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-116">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="53eb8-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-117">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="53eb8-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-118">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="53eb8-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-119">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="53eb8-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-120">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="53eb8-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-121">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="53eb8-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53eb8-122">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="53eb8-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="53eb8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53eb8-123">Requirements</span></span>



| <span data-ttu-id="53eb8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53eb8-124">Requirement</span></span> | <span data-ttu-id="53eb8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53eb8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53eb8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53eb8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53eb8-127">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="53eb8-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="53eb8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53eb8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53eb8-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53eb8-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="53eb8-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53eb8-130">Namespace</span></span><br/>                | <span data-ttu-id="53eb8-131">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="53eb8-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53eb8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="53eb8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53eb8-133"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="53eb8-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53eb8-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53eb8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53eb8-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53eb8-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53eb8-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53eb8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53eb8-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="53eb8-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




