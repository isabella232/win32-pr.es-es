---
description: Modifica una entrada de autorización para un servidor de recuperación.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Método ModifyAuthorizationEntry de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688067"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="da80d-103">Método ModifyAuthorizationEntry de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="da80d-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="da80d-104">Modifica una entrada de autorización para un servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="da80d-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="da80d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da80d-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="da80d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da80d-107">*AuthorizationEntry* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da80d-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da80d-108">Representación de cadena de una instancia de la clase [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define la entrada de autorización que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="da80d-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="da80d-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da80d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da80d-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da80d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da80d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da80d-111">Return value</span></span>

<span data-ttu-id="da80d-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="da80d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="da80d-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="da80d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="da80d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="da80d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="da80d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="da80d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="da80d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="da80d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="da80d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="da80d-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="da80d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="da80d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="da80d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="da80d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="da80d-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="da80d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="da80d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da80d-127">Requirements</span></span>



| <span data-ttu-id="da80d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="da80d-128">Requirement</span></span> | <span data-ttu-id="da80d-129">Value</span><span class="sxs-lookup"><span data-stu-id="da80d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da80d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da80d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="da80d-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="da80d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da80d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da80d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="da80d-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="da80d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da80d-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da80d-134">Namespace</span></span><br/>                | <span data-ttu-id="da80d-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="da80d-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da80d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="da80d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da80d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da80d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da80d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da80d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da80d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da80d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da80d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="da80d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da80d-141">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da80d-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="da80d-142">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da80d-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="da80d-143">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da80d-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="da80d-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="da80d-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

