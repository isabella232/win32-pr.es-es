---
description: Modifica la configuración de seguridad actual de una máquina virtual.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Método ModifySecuritySettings de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670018"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="6d04b-103">Método ModifySecuritySettings de la \_ clase SecurityService de MSVM</span><span class="sxs-lookup"><span data-stu-id="6d04b-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="6d04b-104">Modifica la configuración de seguridad actual de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d04b-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d04b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d04b-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6d04b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d04b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d04b-107">*SecuritySettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d04b-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d04b-108">Nuevos datos de la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d04b-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="6d04b-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d04b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d04b-110">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="6d04b-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="6d04b-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="6d04b-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d04b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d04b-112">Return value</span></span>

<span data-ttu-id="6d04b-113">Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6d04b-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6d04b-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6d04b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6d04b-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="6d04b-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="6d04b-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="6d04b-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="6d04b-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-120">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="6d04b-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6d04b-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6d04b-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6d04b-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6d04b-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6d04b-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6d04b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d04b-125">Requirements</span></span>



| <span data-ttu-id="6d04b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d04b-126">Requirement</span></span> | <span data-ttu-id="6d04b-127">Value</span><span class="sxs-lookup"><span data-stu-id="6d04b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d04b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d04b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6d04b-129">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d04b-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6d04b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d04b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6d04b-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6d04b-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6d04b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6d04b-132">Namespace</span></span><br/>                | <span data-ttu-id="6d04b-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6d04b-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6d04b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6d04b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d04b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d04b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d04b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d04b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d04b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d04b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6d04b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d04b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d04b-139">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="6d04b-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




