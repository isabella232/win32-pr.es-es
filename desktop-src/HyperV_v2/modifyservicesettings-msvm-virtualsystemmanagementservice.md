---
description: Modifica los datos de configuración para el servicio.
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Método ModifyServiceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911677"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="21074-103">Método ModifyServiceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="21074-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="21074-104">Modifica los datos de configuración para el servicio.</span><span class="sxs-lookup"><span data-stu-id="21074-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="21074-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21074-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="21074-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21074-107">*SettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21074-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21074-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="21074-108">Type: **string**</span></span>

<span data-ttu-id="21074-109">Instancia insertada de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) que contiene los aspectos modificados del servicio existente.</span><span class="sxs-lookup"><span data-stu-id="21074-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="21074-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="21074-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21074-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="21074-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="21074-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="21074-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21074-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21074-113">Return value</span></span>

<span data-ttu-id="21074-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21074-114">Type: **uint32**</span></span>

<span data-ttu-id="21074-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="21074-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="21074-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="21074-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="21074-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="21074-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="21074-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="21074-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="21074-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="21074-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="21074-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="21074-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="21074-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="21074-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="21074-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="21074-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="21074-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="21074-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="21074-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="21074-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="21074-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="21074-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="21074-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="21074-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="21074-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="21074-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="21074-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="21074-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="21074-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21074-129">Remarks</span></span>

<span data-ttu-id="21074-130">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="21074-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="21074-131">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="21074-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="21074-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21074-132">Requirements</span></span>



| <span data-ttu-id="21074-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="21074-133">Requirement</span></span> | <span data-ttu-id="21074-134">Value</span><span class="sxs-lookup"><span data-stu-id="21074-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21074-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21074-135">Minimum supported client</span></span><br/> | <span data-ttu-id="21074-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="21074-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="21074-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21074-137">Minimum supported server</span></span><br/> | <span data-ttu-id="21074-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="21074-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21074-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21074-139">Namespace</span></span><br/>                | <span data-ttu-id="21074-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="21074-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="21074-141">MOF</span><span class="sxs-lookup"><span data-stu-id="21074-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21074-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21074-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21074-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21074-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21074-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21074-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21074-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="21074-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21074-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="21074-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="21074-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="21074-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="21074-148">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21074-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

