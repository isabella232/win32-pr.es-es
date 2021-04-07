---
description: Modifica las subredes de la red de migración del servicio de migración del sistema virtual.
ms.assetid: 54ea230a-cda9-4fff-8f79-88f2922b2b15
title: Método ModifyNetworkSettings de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b57cd3ee594bda704c1bd3b6c344c90eb6a1f7fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002486"
---
# <a name="modifynetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="de293-103">Método ModifyNetworkSettings de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="de293-103">ModifyNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="de293-104">Modifica las subredes de la red de migración del servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="de293-104">Modifies migration network subnets of the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="de293-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de293-105">Syntax</span></span>


```mof
uint32 ModifyNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="de293-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de293-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de293-107">*NetworkSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de293-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-108">Una matriz de instancias incrustadas de la clase [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que contienen la configuración de la red de migración.</span><span class="sxs-lookup"><span data-stu-id="de293-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="de293-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="de293-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="de293-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de293-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de293-111">Return value</span></span>

<span data-ttu-id="de293-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="de293-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="de293-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="de293-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="de293-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="de293-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="de293-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="de293-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="de293-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="de293-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="de293-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="de293-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="de293-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="de293-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="de293-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="de293-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="de293-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="de293-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="de293-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="de293-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="de293-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="de293-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="de293-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="de293-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="de293-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="de293-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="de293-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="de293-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="de293-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de293-126">Requirements</span></span>



| <span data-ttu-id="de293-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="de293-127">Requirement</span></span> | <span data-ttu-id="de293-128">Value</span><span class="sxs-lookup"><span data-stu-id="de293-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de293-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de293-129">Minimum supported client</span></span><br/> | <span data-ttu-id="de293-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="de293-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="de293-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de293-131">Minimum supported server</span></span><br/> | <span data-ttu-id="de293-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="de293-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de293-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de293-133">Namespace</span></span><br/>                | <span data-ttu-id="de293-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="de293-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="de293-135">MOF</span><span class="sxs-lookup"><span data-stu-id="de293-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de293-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de293-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de293-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de293-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de293-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de293-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de293-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="de293-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de293-140">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="de293-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="de293-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="de293-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="de293-142">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="de293-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

