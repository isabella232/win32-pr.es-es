---
description: Establece la entrada de autorización de replicación para una máquina virtual.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Método SetAuthorizationEntry de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687468"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="54dba-103">Método SetAuthorizationEntry de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="54dba-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="54dba-104">Establece la entrada de autorización de replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54dba-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="54dba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54dba-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="54dba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54dba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54dba-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54dba-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54dba-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a establecer la entrada de autorización.</span><span class="sxs-lookup"><span data-stu-id="54dba-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="54dba-109">*AuthorizationEntry* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54dba-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54dba-110">Representación de cadena de una instancia de la clase [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) que define la entrada de autorización que se va a usar para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54dba-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="54dba-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54dba-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54dba-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="54dba-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54dba-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54dba-113">Return value</span></span>

<span data-ttu-id="54dba-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="54dba-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="54dba-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="54dba-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="54dba-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="54dba-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="54dba-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="54dba-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="54dba-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="54dba-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="54dba-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="54dba-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="54dba-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="54dba-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="54dba-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="54dba-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="54dba-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="54dba-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="54dba-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54dba-129">Requirements</span></span>



| <span data-ttu-id="54dba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54dba-130">Requirement</span></span> | <span data-ttu-id="54dba-131">Value</span><span class="sxs-lookup"><span data-stu-id="54dba-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54dba-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54dba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="54dba-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="54dba-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="54dba-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54dba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="54dba-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="54dba-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54dba-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54dba-136">Namespace</span></span><br/>                | <span data-ttu-id="54dba-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="54dba-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="54dba-138">MOF</span><span class="sxs-lookup"><span data-stu-id="54dba-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54dba-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54dba-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54dba-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54dba-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54dba-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54dba-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54dba-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="54dba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54dba-143">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="54dba-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="54dba-144">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="54dba-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="54dba-145">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="54dba-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="54dba-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="54dba-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

