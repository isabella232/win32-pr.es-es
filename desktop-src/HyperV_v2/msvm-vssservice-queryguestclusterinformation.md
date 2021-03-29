---
description: Consultar la información del clúster desde el host de Hyper-V hasta el invitado.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Método QueryGuestClusterInformation de la clase Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540262"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="f2b6f-103">Método QueryGuestClusterInformation de la \_ clase VssService de MSVM</span><span class="sxs-lookup"><span data-stu-id="f2b6f-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="f2b6f-104">Consultar la información del clúster desde el host de Hyper-V hasta el invitado.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2b6f-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="f2b6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2b6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b6f-107">*GuestClusterInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2b6f-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b6f-108">Si se ejecuta correctamente, contiene un [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md) que describe el clúster invitado.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b6f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2b6f-109">Return value</span></span>

<span data-ttu-id="f2b6f-110">Si se ejecuta correctamente, devuelve un 0 (completado sin errores) o 4096 (trabajo iniciado). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="f2b6f-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-112">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-113">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-114">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-115">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-116">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-117">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-118">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-119">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-120">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-121">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-122">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f2b6f-123">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f2b6f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2b6f-124">Requirements</span></span>



| <span data-ttu-id="f2b6f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2b6f-125">Requirement</span></span> | <span data-ttu-id="f2b6f-126">Value</span><span class="sxs-lookup"><span data-stu-id="f2b6f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b6f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2b6f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b6f-128">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2b6f-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f2b6f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2b6f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b6f-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f2b6f-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f2b6f-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2b6f-131">Namespace</span></span><br/>                | <span data-ttu-id="f2b6f-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f2b6f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2b6f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f2b6f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2b6f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2b6f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2b6f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2b6f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b6f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2b6f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2b6f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2b6f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b6f-138">**MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="f2b6f-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




