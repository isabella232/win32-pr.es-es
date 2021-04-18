---
description: Agrega la configuración del servicio de invitado a una configuración de sistema virtual.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Método AddGuestServiceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540302"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2fb19-103">Método AddGuestServiceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="2fb19-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2fb19-104">Agrega la configuración del servicio de invitado a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2fb19-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="2fb19-105">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="2fb19-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb19-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fb19-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2fb19-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fb19-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb19-108">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fb19-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb19-109">Referencia a un [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que describe la configuración afectada.</span><span class="sxs-lookup"><span data-stu-id="2fb19-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2fb19-110">*GuestServiceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fb19-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb19-111">Una matriz que contiene la configuración del servicio de invitado.</span><span class="sxs-lookup"><span data-stu-id="2fb19-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="2fb19-112">*ResultingGuestServiceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2fb19-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb19-113">Si se ejecuta correctamente, contiene una referencia a un [**\_ SettingData de CIM**](cim-settingdata.md) que describe la configuración del servicio invitado resultante.</span><span class="sxs-lookup"><span data-stu-id="2fb19-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="2fb19-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2fb19-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb19-115">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fb19-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb19-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fb19-116">Return value</span></span>

<span data-ttu-id="2fb19-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2fb19-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2fb19-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2fb19-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-119">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2fb19-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-120">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="2fb19-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-121">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="2fb19-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-122">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="2fb19-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2fb19-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2fb19-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2fb19-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2fb19-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="2fb19-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2fb19-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fb19-127">Requirements</span></span>



| <span data-ttu-id="2fb19-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb19-128">Requirement</span></span> | <span data-ttu-id="2fb19-129">Value</span><span class="sxs-lookup"><span data-stu-id="2fb19-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb19-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb19-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb19-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fb19-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2fb19-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb19-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb19-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2fb19-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2fb19-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2fb19-134">Namespace</span></span><br/>                | <span data-ttu-id="2fb19-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2fb19-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2fb19-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2fb19-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fb19-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fb19-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fb19-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fb19-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb19-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fb19-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2fb19-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fb19-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb19-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="2fb19-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

