---
description: Recupera el error.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Método GetError de la clase Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911014"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="08995-103">Método GetError de la \_ clase StorageJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="08995-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="08995-104">Recupera el error.</span><span class="sxs-lookup"><span data-stu-id="08995-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="08995-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08995-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="08995-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08995-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08995-107">*Error* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="08995-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08995-108">El error recuperado.</span><span class="sxs-lookup"><span data-stu-id="08995-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08995-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08995-109">Return value</span></span>

<span data-ttu-id="08995-110">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="08995-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="08995-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="08995-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08995-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="08995-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="08995-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="08995-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="08995-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="08995-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="08995-115">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="08995-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="08995-116">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="08995-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="08995-117">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="08995-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="08995-118">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="08995-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="08995-119">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="08995-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="08995-120">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="08995-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="08995-121">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="08995-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="08995-122">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="08995-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="08995-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08995-123">Requirements</span></span>



| <span data-ttu-id="08995-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08995-124">Requirement</span></span> | <span data-ttu-id="08995-125">Value</span><span class="sxs-lookup"><span data-stu-id="08995-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08995-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08995-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08995-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="08995-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="08995-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08995-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08995-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08995-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="08995-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08995-130">Namespace</span></span><br/>                | <span data-ttu-id="08995-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="08995-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="08995-132">MOF</span><span class="sxs-lookup"><span data-stu-id="08995-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08995-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08995-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08995-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08995-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08995-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08995-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08995-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="08995-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08995-137">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="08995-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




