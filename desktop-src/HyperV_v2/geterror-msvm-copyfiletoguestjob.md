---
description: 'Msvm_CopyFileToGuestJob método::GetError: recupera el objeto de error para el trabajo, si existe alguno.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob::GetError (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119373"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="3b6e0-103">Método Msvm \_ CopyFileToGuestJob::GetError</span><span class="sxs-lookup"><span data-stu-id="3b6e0-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="3b6e0-104">Recupera el objeto de error para el trabajo, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="3b6e0-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="3b6e0-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un [**objeto \_ error CIM.**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b6e0-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="3b6e0-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelve una instancia **\_ de error** de CIM.</span><span class="sxs-lookup"><span data-stu-id="3b6e0-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6e0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b6e0-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="3b6e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b6e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6e0-109">*Error* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b6e0-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6e0-110">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una instancia incrustada de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="3b6e0-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="3b6e0-111">Si el estado operativo del trabajo es 2 (correcto), **se devuelve Null.**</span><span class="sxs-lookup"><span data-stu-id="3b6e0-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6e0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b6e0-112">Return value</span></span>

<span data-ttu-id="3b6e0-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b6e0-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3b6e0-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-118">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-119">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-120">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-121">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-124">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3b6e0-125">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="3b6e0-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3b6e0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b6e0-126">Requirements</span></span>



| <span data-ttu-id="3b6e0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b6e0-127">Requirement</span></span> | <span data-ttu-id="3b6e0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3b6e0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6e0-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b6e0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6e0-130">Windows 8.1 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3b6e0-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3b6e0-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b6e0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6e0-132">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b6e0-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3b6e0-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b6e0-133">Namespace</span></span><br/>                | <span data-ttu-id="3b6e0-134">\\\\Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b6e0-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="3b6e0-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3b6e0-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b6e0-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b6e0-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b6e0-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b6e0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b6e0-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b6e0-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b6e0-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3b6e0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6e0-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="3b6e0-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

