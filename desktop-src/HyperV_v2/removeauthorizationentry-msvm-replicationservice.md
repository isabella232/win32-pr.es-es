---
description: Quita una entrada de autorización de un servidor de recuperación.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Método RemoveAuthorizationEntry de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688550"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="58543-103">Método RemoveAuthorizationEntry de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="58543-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="58543-104">Quita una entrada de autorización de un servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="58543-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="58543-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58543-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="58543-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58543-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58543-107">*AllowedPrimaryHostSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58543-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58543-108">El servidor principal para el que se va a quitar la entrada de autorización del servidor.</span><span class="sxs-lookup"><span data-stu-id="58543-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="58543-109">Es igual que la propiedad **AllowedPrimaryHostSystem** de la clase [**\_ ReplicationAuthorizationSettingData de MSVM**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="58543-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="58543-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58543-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58543-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58543-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58543-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58543-112">Return value</span></span>

<span data-ttu-id="58543-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="58543-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="58543-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="58543-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58543-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="58543-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="58543-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="58543-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="58543-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="58543-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="58543-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="58543-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="58543-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="58543-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="58543-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="58543-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="58543-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="58543-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="58543-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="58543-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="58543-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="58543-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="58543-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="58543-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="58543-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="58543-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="58543-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="58543-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="58543-127">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="58543-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="58543-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58543-128">Remarks</span></span>

<span data-ttu-id="58543-129">Si se quita una entrada de autorización, se detendrá la replicación de todas las máquinas virtuales que estén autorizadas con la entrada.</span><span class="sxs-lookup"><span data-stu-id="58543-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="58543-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58543-130">Requirements</span></span>



| <span data-ttu-id="58543-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58543-131">Requirement</span></span> | <span data-ttu-id="58543-132">Value</span><span class="sxs-lookup"><span data-stu-id="58543-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58543-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58543-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58543-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="58543-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58543-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58543-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58543-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="58543-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58543-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58543-137">Namespace</span></span><br/>                | <span data-ttu-id="58543-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="58543-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58543-139">MOF</span><span class="sxs-lookup"><span data-stu-id="58543-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58543-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58543-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58543-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58543-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58543-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58543-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58543-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="58543-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58543-144">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="58543-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="58543-145">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="58543-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="58543-146">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="58543-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="58543-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="58543-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

