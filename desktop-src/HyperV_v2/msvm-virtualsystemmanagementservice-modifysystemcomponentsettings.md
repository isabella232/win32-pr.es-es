---
description: Modifica la configuración genérica del componente del sistema.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Método ModifySystemComponentSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686590"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="04090-103">Método ModifySystemComponentSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="04090-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="04090-104">Modifica la configuración genérica del componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="04090-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="04090-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04090-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="04090-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04090-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04090-107">*ComponentSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04090-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04090-108">Matriz de valores de componentes que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="04090-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="04090-109">*ResultingComponentSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="04090-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04090-110">Si se ejecuta correctamente, devuelve una matriz de [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) que hace referencia a la configuración del componente resultante.</span><span class="sxs-lookup"><span data-stu-id="04090-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="04090-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="04090-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04090-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04090-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04090-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04090-113">Return value</span></span>

<span data-ttu-id="04090-114">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="04090-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="04090-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="04090-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04090-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="04090-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04090-117">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="04090-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04090-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="04090-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04090-119">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="04090-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04090-120">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="04090-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="04090-121">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="04090-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="04090-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04090-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04090-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="04090-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="04090-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="04090-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="04090-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="04090-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="04090-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04090-126">Requirements</span></span>



| <span data-ttu-id="04090-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04090-127">Requirement</span></span> | <span data-ttu-id="04090-128">Value</span><span class="sxs-lookup"><span data-stu-id="04090-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04090-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04090-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04090-130">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="04090-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04090-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04090-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04090-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04090-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="04090-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="04090-133">Namespace</span></span><br/>                | <span data-ttu-id="04090-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="04090-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="04090-135">MOF</span><span class="sxs-lookup"><span data-stu-id="04090-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04090-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04090-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04090-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04090-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04090-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04090-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04090-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="04090-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04090-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="04090-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

