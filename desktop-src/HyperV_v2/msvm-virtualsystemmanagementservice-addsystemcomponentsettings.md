---
description: Agrega la configuración genérica a una configuración de sistema virtual.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Método AddSystemComponentSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686592"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="63342-103">Método AddSystemComponentSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="63342-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="63342-104">Agrega la configuración genérica a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="63342-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="63342-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63342-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="63342-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63342-107">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63342-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="63342-108">*ComponentSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63342-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63342-109">Configuración del componente que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="63342-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="63342-110">*ResultingComponentSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63342-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63342-111">Si se ejecuta correctamente, hace referencia a un [**\_ SystemComponentSettingData de MSVM**](msvm-systemcomponentsettingdata.md) que contiene la configuración del componente resultante.</span><span class="sxs-lookup"><span data-stu-id="63342-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="63342-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63342-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63342-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63342-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63342-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63342-114">Return value</span></span>

<span data-ttu-id="63342-115">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="63342-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="63342-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="63342-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63342-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="63342-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63342-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="63342-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63342-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="63342-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63342-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="63342-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63342-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="63342-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63342-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="63342-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="63342-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="63342-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="63342-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="63342-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="63342-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63342-125">Requirements</span></span>



| <span data-ttu-id="63342-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63342-126">Requirement</span></span> | <span data-ttu-id="63342-127">Value</span><span class="sxs-lookup"><span data-stu-id="63342-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63342-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63342-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63342-129">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="63342-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63342-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63342-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63342-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="63342-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="63342-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63342-132">Namespace</span></span><br/>                | <span data-ttu-id="63342-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="63342-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="63342-134">MOF</span><span class="sxs-lookup"><span data-stu-id="63342-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63342-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63342-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63342-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63342-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63342-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63342-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63342-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="63342-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63342-139">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="63342-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

