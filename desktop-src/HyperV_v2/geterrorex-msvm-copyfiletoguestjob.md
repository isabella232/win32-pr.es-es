---
description: Recupera los objetos de error del trabajo, si existen.
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: 'Msvm_CopyFileToGuestJob:: GetErrorEx (método)'
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
ms.openlocfilehash: 179ad3a70a985442d855d447ef4eab955d177f0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666554"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="9b0e3-103">MSVM \_ CopyFileToGuestJob:: GetErrorEx (método)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="9b0e3-104">Recupera los objetos de error del trabajo, si existen.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="9b0e3-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="9b0e3-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="9b0e3-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="9b0e3-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b0e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b0e3-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="9b0e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b0e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b0e3-109">*Errores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b0e3-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b0e3-110">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) , en formato CIM-XML, que representan los errores encontrados en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="9b0e3-111">Si el estado operativo del trabajo es 2 (correcto), se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="9b0e3-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b0e3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b0e3-112">Return value</span></span>

<span data-ttu-id="9b0e3-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9b0e3-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9b0e3-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9b0e3-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9b0e3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b0e3-126">Requirements</span></span>



| <span data-ttu-id="9b0e3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b0e3-127">Requirement</span></span> | <span data-ttu-id="9b0e3-128">Value</span><span class="sxs-lookup"><span data-stu-id="9b0e3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0e3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b0e3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9b0e3-130">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9b0e3-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9b0e3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b0e3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9b0e3-132">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b0e3-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9b0e3-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b0e3-133">Namespace</span></span><br/>                | <span data-ttu-id="9b0e3-134">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9b0e3-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="9b0e3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9b0e3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b0e3-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b0e3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b0e3-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b0e3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b0e3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b0e3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b0e3-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b0e3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0e3-140">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




