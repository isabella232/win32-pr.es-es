---
description: Quita la configuración del servicio de invitado de una configuración de sistema virtual.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Método RemoveGuestServiceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686586"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f28fa-103">Método RemoveGuestServiceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="f28fa-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f28fa-104">Quita la configuración del servicio de invitado de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f28fa-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="f28fa-105">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="f28fa-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28fa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f28fa-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f28fa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f28fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28fa-108">*GuestServiceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f28fa-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28fa-109">Referencia a una matriz de [**un \_ SettingData de CIM**](cim-settingdata.md) que describe la configuración del servicio de invitado que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="f28fa-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="f28fa-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f28fa-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f28fa-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f28fa-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28fa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f28fa-112">Return value</span></span>

<span data-ttu-id="f28fa-113">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f28fa-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f28fa-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f28fa-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="f28fa-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="f28fa-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="f28fa-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="f28fa-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="f28fa-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f28fa-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f28fa-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f28fa-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f28fa-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f28fa-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f28fa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f28fa-124">Requirements</span></span>



| <span data-ttu-id="f28fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f28fa-125">Requirement</span></span> | <span data-ttu-id="f28fa-126">Value</span><span class="sxs-lookup"><span data-stu-id="f28fa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f28fa-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f28fa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f28fa-128">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f28fa-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f28fa-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f28fa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f28fa-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f28fa-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f28fa-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f28fa-131">Namespace</span></span><br/>                | <span data-ttu-id="f28fa-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f28fa-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f28fa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f28fa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f28fa-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f28fa-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f28fa-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f28fa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f28fa-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f28fa-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f28fa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f28fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28fa-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f28fa-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

