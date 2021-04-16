---
description: Recupera el objeto de error del trabajo, si existe uno.
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Msvm_CopyFileToGuestJob:: GetError (método)'
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
ms.openlocfilehash: a0a89feab4e78ba3703e117972598c4de5f70310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686890"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="c8e72-103">MSVM \_ CopyFileToGuestJob:: GetError (método)</span><span class="sxs-lookup"><span data-stu-id="c8e72-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="c8e72-104">Recupera el objeto de error del trabajo, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="c8e72-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="c8e72-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un objeto de [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c8e72-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="c8e72-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelve una instancia de **\_ error de CIM** .</span><span class="sxs-lookup"><span data-stu-id="c8e72-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e72-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e72-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="c8e72-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8e72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e72-109">*Error* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8e72-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e72-110">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una instancia incrustada de la clase de [**\_ error MSVM**](msvm-error.md) , en formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="c8e72-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="c8e72-111">Si el estado operativo del trabajo es 2 (correcto), se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="c8e72-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e72-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8e72-112">Return value</span></span>

<span data-ttu-id="c8e72-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8e72-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c8e72-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c8e72-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c8e72-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c8e72-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c8e72-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c8e72-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c8e72-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c8e72-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c8e72-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="c8e72-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c8e72-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c8e72-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c8e72-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c8e72-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c8e72-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e72-126">Requirements</span></span>



| <span data-ttu-id="c8e72-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e72-127">Requirement</span></span> | <span data-ttu-id="c8e72-128">Value</span><span class="sxs-lookup"><span data-stu-id="c8e72-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e72-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e72-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e72-130">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="c8e72-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c8e72-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e72-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e72-132">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8e72-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8e72-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8e72-133">Namespace</span></span><br/>                | <span data-ttu-id="c8e72-134">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c8e72-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c8e72-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c8e72-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8e72-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8e72-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8e72-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8e72-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8e72-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8e72-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8e72-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8e72-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e72-140">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="c8e72-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

