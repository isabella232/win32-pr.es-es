---
description: Restaura de nuevo al último protector de clave válido conocido.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Método RestoreLastKnownGoodKeyProtector de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689575"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="930a3-103">Método RestoreLastKnownGoodKeyProtector de la \_ clase SecurityService de MSVM</span><span class="sxs-lookup"><span data-stu-id="930a3-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="930a3-104">Restaura de nuevo al último protector de clave válido conocido.</span><span class="sxs-lookup"><span data-stu-id="930a3-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="930a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="930a3-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="930a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="930a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930a3-107">*SecuritySettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930a3-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930a3-108">String contiene una instancia incrustada de la clase [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="930a3-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="930a3-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="930a3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="930a3-110">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="930a3-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="930a3-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="930a3-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930a3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="930a3-112">Return value</span></span>

<span data-ttu-id="930a3-113">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="930a3-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="930a3-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="930a3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="930a3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="930a3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="930a3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="930a3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="930a3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="930a3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="930a3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="930a3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="930a3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="930a3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="930a3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="930a3-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="930a3-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="930a3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="930a3-127">Requirements</span></span>



| <span data-ttu-id="930a3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="930a3-128">Requirement</span></span> | <span data-ttu-id="930a3-129">Value</span><span class="sxs-lookup"><span data-stu-id="930a3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930a3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="930a3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="930a3-131">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="930a3-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="930a3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="930a3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="930a3-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="930a3-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="930a3-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="930a3-134">Namespace</span></span><br/>                | <span data-ttu-id="930a3-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="930a3-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="930a3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="930a3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="930a3-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="930a3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="930a3-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="930a3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="930a3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="930a3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="930a3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="930a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930a3-141">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="930a3-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




