---
description: Agrega subredes de red de migración para el servicio de migración del sistema virtual.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Método AddNetworkSettings de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667479"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="c139c-103">Método AddNetworkSettings de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="c139c-103">AddNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="c139c-104">Agrega subredes de red de migración para el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="c139c-104">Adds migration network subnets for the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c139c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c139c-105">Syntax</span></span>


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c139c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c139c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c139c-107">*NetworkSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c139c-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c139c-108">Una matriz de instancias incrustadas de la clase [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que contienen la configuración de la red de migración.</span><span class="sxs-lookup"><span data-stu-id="c139c-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="c139c-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c139c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c139c-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c139c-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c139c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c139c-111">Return value</span></span>

<span data-ttu-id="c139c-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c139c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c139c-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c139c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c139c-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c139c-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c139c-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c139c-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c139c-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c139c-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c139c-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c139c-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="c139c-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c139c-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c139c-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c139c-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c139c-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c139c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c139c-126">Requirements</span></span>



| <span data-ttu-id="c139c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c139c-127">Requirement</span></span> | <span data-ttu-id="c139c-128">Value</span><span class="sxs-lookup"><span data-stu-id="c139c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c139c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c139c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c139c-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c139c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c139c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c139c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c139c-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c139c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c139c-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c139c-133">Namespace</span></span><br/>                | <span data-ttu-id="c139c-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c139c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c139c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c139c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c139c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c139c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c139c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c139c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c139c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c139c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c139c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c139c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c139c-140">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="c139c-140">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="c139c-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="c139c-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="c139c-142">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="c139c-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

