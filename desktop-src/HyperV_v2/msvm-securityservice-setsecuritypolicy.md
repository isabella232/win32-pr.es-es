---
description: 'Método SetSecurityPolicy de la clase Msvm_SecurityService : establece el protector de clave para un sistema virtual.'
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Método SetSecurityPolicy de la Msvm_SecurityService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118733"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="60127-103">Método SetSecurityPolicy de la clase SecurityService de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="60127-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="60127-104">Establece el protector de clave para un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60127-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="60127-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60127-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="60127-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60127-107">*SecuritySettingData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="60127-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60127-108">String contiene una instancia incrustada de la [**clase \_ SecuritySettingData de Msvm**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60127-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="60127-109">*SecurityPolicy* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="60127-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60127-110">Matriz de bytes sin formato que contiene la directiva de seguridad que se establece.</span><span class="sxs-lookup"><span data-stu-id="60127-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="60127-111">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60127-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60127-112">Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="60127-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="60127-113">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="60127-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60127-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60127-114">Return value</span></span>

<span data-ttu-id="60127-115">On, success, devuelve un valor de 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="60127-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="60127-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="60127-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60127-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="60127-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="60127-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="60127-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="60127-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="60127-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="60127-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="60127-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="60127-121">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="60127-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="60127-122">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="60127-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="60127-123">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="60127-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="60127-124">**El sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="60127-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="60127-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="60127-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="60127-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="60127-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="60127-127">**El sistema no está** disponible (32777)</span><span class="sxs-lookup"><span data-stu-id="60127-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="60127-128">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="60127-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="60127-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60127-129">Requirements</span></span>



| <span data-ttu-id="60127-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="60127-130">Requirement</span></span> | <span data-ttu-id="60127-131">Valor</span><span class="sxs-lookup"><span data-stu-id="60127-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60127-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60127-132">Minimum supported client</span></span><br/> | <span data-ttu-id="60127-133">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="60127-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60127-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60127-134">Minimum supported server</span></span><br/> | <span data-ttu-id="60127-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60127-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="60127-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60127-136">Namespace</span></span><br/>                | <span data-ttu-id="60127-137">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="60127-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60127-138">MOF</span><span class="sxs-lookup"><span data-stu-id="60127-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60127-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="60127-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60127-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60127-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60127-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60127-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60127-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60127-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60127-143">**SecurityService de Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="60127-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




