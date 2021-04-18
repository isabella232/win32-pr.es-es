---
description: Establece el protector de clave para un sistema virtual.
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Método SetKeyProtector de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 404baf0a529a6e96869fbcd355a81308f5d1e966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666677"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="568bd-103">Método SetKeyProtector de la \_ clase SecurityService de MSVM</span><span class="sxs-lookup"><span data-stu-id="568bd-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="568bd-104">Establece el protector de clave para un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="568bd-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="568bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="568bd-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="568bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="568bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568bd-107">*SecuritySettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="568bd-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="568bd-108">String contiene una instancia incrustada de la clase [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="568bd-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="568bd-109">*KeyProtector* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="568bd-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="568bd-110">Matriz de bytes sin formato que contiene el protector de clave que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="568bd-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="568bd-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="568bd-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="568bd-112">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="568bd-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="568bd-113">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="568bd-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568bd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="568bd-114">Return value</span></span>

<span data-ttu-id="568bd-115">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="568bd-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="568bd-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="568bd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="568bd-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="568bd-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="568bd-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="568bd-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="568bd-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="568bd-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="568bd-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="568bd-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="568bd-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="568bd-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="568bd-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="568bd-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="568bd-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="568bd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="568bd-129">Requirements</span></span>



| <span data-ttu-id="568bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="568bd-130">Requirement</span></span> | <span data-ttu-id="568bd-131">Value</span><span class="sxs-lookup"><span data-stu-id="568bd-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="568bd-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="568bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="568bd-133">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="568bd-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="568bd-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="568bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="568bd-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="568bd-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="568bd-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="568bd-136">Namespace</span></span><br/>                | <span data-ttu-id="568bd-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="568bd-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="568bd-138">MOF</span><span class="sxs-lookup"><span data-stu-id="568bd-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="568bd-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="568bd-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="568bd-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="568bd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="568bd-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="568bd-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="568bd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="568bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="568bd-143">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="568bd-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




