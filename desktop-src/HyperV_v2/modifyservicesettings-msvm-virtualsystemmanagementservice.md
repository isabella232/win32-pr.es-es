---
description: 'Método ModifyServiceSettings de la Msvm_VirtualSystemManagementService : modifica los datos de configuración del servicio.'
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Método ModifyServiceSettings de la Msvm_VirtualSystemManagementService clase
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
ms.openlocfilehash: ee4e8ae904292bae06770f23cf6c853d5e5448bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112173"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6e3a3-103">Método ModifyServiceSettings de la clase Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="6e3a3-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6e3a3-104">Modifica los datos de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3a3-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e3a3-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6e3a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e3a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e3a3-107">*SettingData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3a3-108">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-108">Type: **string**</span></span>

<span data-ttu-id="6e3a3-109">Instancia incrustada de la [**clase Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) que contiene los aspectos modificados del servicio existente.</span><span class="sxs-lookup"><span data-stu-id="6e3a3-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3a3-110">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3a3-111">Tipo: **[ **Cim \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="6e3a3-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6e3a3-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e3a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e3a3-113">Return value</span></span>

<span data-ttu-id="6e3a3-114">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-114">Type: **uint32**</span></span>

<span data-ttu-id="6e3a3-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6e3a3-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6e3a3-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-121">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-122">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-123">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-124">**El sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-127">**El sistema no está** disponible (32777)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6e3a3-128">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6e3a3-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e3a3-129">Remarks</span></span>

<span data-ttu-id="6e3a3-130">El acceso a la [**clase \_ VirtualSystemManagementService de Msvm**](msvm-virtualsystemmanagementservice.md) podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="6e3a3-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6e3a3-131">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="6e3a3-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e3a3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e3a3-132">Requirements</span></span>



| <span data-ttu-id="6e3a3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e3a3-133">Requirement</span></span> | <span data-ttu-id="6e3a3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6e3a3-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3a3-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e3a3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3a3-136">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6e3a3-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e3a3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3a3-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e3a3-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e3a3-139">Namespace</span></span><br/>                | <span data-ttu-id="6e3a3-140">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="6e3a3-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6e3a3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6e3a3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e3a3-142"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e3a3-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e3a3-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e3a3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e3a3-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e3a3-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e3a3-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e3a3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3a3-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="6e3a3-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="6e3a3-148">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e3a3-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

