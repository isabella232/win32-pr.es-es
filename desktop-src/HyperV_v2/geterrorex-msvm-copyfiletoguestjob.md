---
description: 'Msvm_CopyFileToGuestJob::GetErrorEx: recupera los objetos de error para el trabajo, si existe alguno.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob::GetErrorEx (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109673"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="862ee-103">Método Msvm \_ CopyFileToGuestJob::GetErrorEx</span><span class="sxs-lookup"><span data-stu-id="862ee-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="862ee-104">Recupera los objetos de error del trabajo, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="862ee-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="862ee-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna [**instancia de \_ error de Msvm.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="862ee-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="862ee-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelven una o varias instancias de error de **Msvm. \_**</span><span class="sxs-lookup"><span data-stu-id="862ee-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="862ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="862ee-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="862ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="862ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862ee-109">*Errores* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="862ee-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862ee-110">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML, que representan los errores encontrados en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="862ee-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="862ee-111">Si el estado operativo del trabajo es 2 (correcto), se **devuelve Null.**</span><span class="sxs-lookup"><span data-stu-id="862ee-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862ee-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="862ee-112">Return value</span></span>

<span data-ttu-id="862ee-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="862ee-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="862ee-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="862ee-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="862ee-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="862ee-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="862ee-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-118">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="862ee-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-119">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="862ee-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-120">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="862ee-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-121">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="862ee-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="862ee-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="862ee-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-124">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="862ee-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="862ee-125">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="862ee-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="862ee-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="862ee-126">Requirements</span></span>



| <span data-ttu-id="862ee-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="862ee-127">Requirement</span></span> | <span data-ttu-id="862ee-128">Valor</span><span class="sxs-lookup"><span data-stu-id="862ee-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="862ee-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="862ee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="862ee-130">Windows 8.1 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="862ee-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="862ee-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="862ee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="862ee-132">Solo aplicaciones de escritorio de Windows Server 2012 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="862ee-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="862ee-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="862ee-133">Namespace</span></span><br/>                | <span data-ttu-id="862ee-134">\\\\Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="862ee-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="862ee-135">MOF</span><span class="sxs-lookup"><span data-stu-id="862ee-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="862ee-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="862ee-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="862ee-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="862ee-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="862ee-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="862ee-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="862ee-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="862ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862ee-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="862ee-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




