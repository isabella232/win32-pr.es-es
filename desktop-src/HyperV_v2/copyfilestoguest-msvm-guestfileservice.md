---
description: Copia archivos del host de Hyper-V a la máquina virtual.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Msvm_GuestFileService:: CopyFilesToGuest (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667837"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="2d71d-103">MSVM \_ GuestFileService:: CopyFilesToGuest (método)</span><span class="sxs-lookup"><span data-stu-id="2d71d-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="2d71d-104">Copia archivos del host de Hyper-V a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2d71d-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d71d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d71d-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="2d71d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d71d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d71d-107">*CopyFileToGuestSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d71d-108">Una matriz de instancias de la clase [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) que representa un trabajo de operación del servicio de archivos invitados.</span><span class="sxs-lookup"><span data-stu-id="2d71d-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="2d71d-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d71d-110">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="2d71d-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="2d71d-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="2d71d-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="2d71d-112">Este parámetro se agregó en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d71d-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="2d71d-113">*ParentPools* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d71d-114">Una matriz opcional de referencias de [**\_ CopyFileToGuestJob de MSVM**](msvm-copyfiletoguestjob.md) que se usan para supervisar el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="2d71d-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="2d71d-115">**CopyFilesToGuest** usa *ParentPools* si no se puede ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="2d71d-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="2d71d-116">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="2d71d-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="2d71d-117">Este parámetro se quitó en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d71d-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d71d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d71d-118">Return value</span></span>

<span data-ttu-id="2d71d-119">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un valor de error.</span><span class="sxs-lookup"><span data-stu-id="2d71d-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="2d71d-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2d71d-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2d71d-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-122">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2d71d-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-123">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2d71d-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-124">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2d71d-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-125">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2d71d-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-126">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2d71d-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-127">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2d71d-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-128">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2d71d-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-129">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2d71d-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-130">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2d71d-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-131">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2d71d-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2d71d-132">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2d71d-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2d71d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d71d-133">Requirements</span></span>



| <span data-ttu-id="2d71d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d71d-134">Requirement</span></span> | <span data-ttu-id="2d71d-135">Value</span><span class="sxs-lookup"><span data-stu-id="2d71d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d71d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d71d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2d71d-137">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2d71d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d71d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2d71d-139">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d71d-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d71d-140">Namespace</span></span><br/>                | <span data-ttu-id="2d71d-141">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2d71d-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="2d71d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2d71d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d71d-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d71d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d71d-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d71d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d71d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d71d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d71d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d71d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d71d-147">**MSVM \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="2d71d-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




