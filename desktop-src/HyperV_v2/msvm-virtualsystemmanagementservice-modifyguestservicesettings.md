---
description: Modifica la configuración del servicio de invitado.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Método ModifyGuestServiceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907697"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f3199-103">Método ModifyGuestServiceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="f3199-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f3199-104">Modifica la configuración del servicio de invitado.</span><span class="sxs-lookup"><span data-stu-id="f3199-104">Modifies guest service settings.</span></span>

<span data-ttu-id="f3199-105">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="f3199-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3199-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3199-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f3199-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3199-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3199-108">*GuestServiceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3199-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3199-109">Una matriz que contiene la nueva configuración del servicio de invitado.</span><span class="sxs-lookup"><span data-stu-id="f3199-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="f3199-110">*ResultingGuestServiceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f3199-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3199-111">Si se ejecuta correctamente, contiains una matriz de [**\_ SettingData de CIM**](cim-settingdata.md) que haga referencia a la configuración del servicio de invitado resultante.</span><span class="sxs-lookup"><span data-stu-id="f3199-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="f3199-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f3199-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3199-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3199-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3199-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3199-114">Return value</span></span>

<span data-ttu-id="f3199-115">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f3199-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f3199-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f3199-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="f3199-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="f3199-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="f3199-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="f3199-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="f3199-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="f3199-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f3199-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f3199-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f3199-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f3199-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f3199-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f3199-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3199-127">Requirements</span></span>



| <span data-ttu-id="f3199-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3199-128">Requirement</span></span> | <span data-ttu-id="f3199-129">Value</span><span class="sxs-lookup"><span data-stu-id="f3199-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3199-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3199-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3199-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3199-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f3199-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3199-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3199-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3199-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f3199-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3199-134">Namespace</span></span><br/>                | <span data-ttu-id="f3199-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f3199-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3199-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f3199-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3199-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3199-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3199-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3199-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3199-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3199-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3199-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3199-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3199-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f3199-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

