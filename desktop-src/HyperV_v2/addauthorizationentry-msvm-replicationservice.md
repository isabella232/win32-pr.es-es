---
description: Agrega una entrada de autorización a un servidor de recuperación.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Método AddAuthorizationEntry de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687533"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="4f6e6-103">Método AddAuthorizationEntry de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="4f6e6-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="4f6e6-104">Agrega una entrada de autorización a un servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4f6e6-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="4f6e6-105">Estas entradas se usan para autorizar las conexiones con el servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4f6e6-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f6e6-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4f6e6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f6e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f6e6-108">*AuthorizationEntry* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f6e6-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f6e6-109">Representación de cadena de una instancia de la clase [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define la entrada de autorización que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4f6e6-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="4f6e6-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4f6e6-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f6e6-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f6e6-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f6e6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f6e6-112">Return value</span></span>

<span data-ttu-id="4f6e6-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4f6e6-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4f6e6-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4f6e6-127">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="4f6e6-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4f6e6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f6e6-128">Requirements</span></span>



| <span data-ttu-id="4f6e6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f6e6-129">Requirement</span></span> | <span data-ttu-id="4f6e6-130">Value</span><span class="sxs-lookup"><span data-stu-id="4f6e6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6e6-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f6e6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6e6-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f6e6-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f6e6-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f6e6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6e6-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f6e6-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f6e6-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f6e6-135">Namespace</span></span><br/>                | <span data-ttu-id="4f6e6-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4f6e6-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f6e6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4f6e6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f6e6-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e6-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f6e6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f6e6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f6e6-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e6-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f6e6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f6e6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6e6-142">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="4f6e6-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="4f6e6-143">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="4f6e6-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="4f6e6-144">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="4f6e6-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="4f6e6-145">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="4f6e6-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

