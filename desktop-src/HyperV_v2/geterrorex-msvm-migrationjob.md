---
description: Recupera los objetos de error para el trabajo de migración, si existe alguno.
ms.assetid: 8526e28c-bfc8-42b3-850c-0a875a52a42c
title: Método GetErrorEx de la clase Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b51bc0c439add0e0959d3fd375fad477e51ba35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686888"
---
# <a name="geterrorex-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="ff97b-103">Método GetErrorEx de la \_ clase MigrationJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="ff97b-103">GetErrorEx method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="ff97b-104">Recupera los objetos de error para el trabajo de migración, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="ff97b-104">Retrieves the error objects for the migration job, if any exist.</span></span> <span data-ttu-id="ff97b-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="ff97b-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="ff97b-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="ff97b-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff97b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff97b-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="ff97b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff97b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff97b-109">*Errores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ff97b-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff97b-110">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) , en formato CIM-XML, que representan los errores encontrados en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="ff97b-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="ff97b-111">Si el estado operativo del trabajo es 2 (correcto), se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="ff97b-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff97b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff97b-112">Return value</span></span>

<span data-ttu-id="ff97b-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff97b-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ff97b-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ff97b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff97b-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff97b-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff97b-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff97b-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ff97b-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ff97b-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ff97b-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ff97b-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ff97b-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ff97b-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ff97b-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ff97b-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ff97b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff97b-126">Requirements</span></span>



| <span data-ttu-id="ff97b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff97b-127">Requirement</span></span> | <span data-ttu-id="ff97b-128">Value</span><span class="sxs-lookup"><span data-stu-id="ff97b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff97b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff97b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff97b-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff97b-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff97b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff97b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff97b-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff97b-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff97b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff97b-133">Namespace</span></span><br/>                | <span data-ttu-id="ff97b-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ff97b-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff97b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ff97b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff97b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff97b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff97b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff97b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff97b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff97b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff97b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff97b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff97b-140">**MSVM \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="ff97b-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




