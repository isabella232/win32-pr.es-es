---
description: 'Método GetError de la Msvm_StorageJob : recupera el error.'
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Método GetError de la Msvm_StorageJob clase
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
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109603"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="5721b-103">Método GetError de la clase StorageJob de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="5721b-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="5721b-104">Recupera el error.</span><span class="sxs-lookup"><span data-stu-id="5721b-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="5721b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5721b-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="5721b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5721b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5721b-107">*Error* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5721b-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5721b-108">Error recuperado.</span><span class="sxs-lookup"><span data-stu-id="5721b-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5721b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5721b-109">Return value</span></span>

<span data-ttu-id="5721b-110">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5721b-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5721b-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="5721b-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="5721b-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5721b-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="5721b-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-115">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5721b-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-116">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="5721b-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-117">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="5721b-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-118">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5721b-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-119">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="5721b-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-120">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5721b-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-121">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5721b-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5721b-122">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="5721b-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5721b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5721b-123">Requirements</span></span>



| <span data-ttu-id="5721b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5721b-124">Requirement</span></span> | <span data-ttu-id="5721b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5721b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5721b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5721b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5721b-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5721b-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5721b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5721b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5721b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5721b-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5721b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5721b-130">Namespace</span></span><br/>                | <span data-ttu-id="5721b-131">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="5721b-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5721b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5721b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5721b-133"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="5721b-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5721b-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5721b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5721b-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5721b-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5721b-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5721b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5721b-137">**Msvm \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="5721b-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




