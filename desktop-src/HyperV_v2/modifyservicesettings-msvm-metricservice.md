---
description: Modifica los datos de configuración para el servicio.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810316"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="b9dd0-103">Método ModifyServiceSettings de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b9dd0-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="b9dd0-104">Modifica los datos de configuración para el servicio.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9dd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9dd0-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b9dd0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9dd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9dd0-107">*SettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9dd0-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9dd0-108">Contiene una instancia incrustada de la clase [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="b9dd0-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9dd0-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9dd0-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9dd0-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9dd0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9dd0-111">Return value</span></span>

<span data-ttu-id="b9dd0-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="b9dd0-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9dd0-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="b9dd0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9dd0-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b9dd0-115"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="b9dd0-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="b9dd0-117"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="b9dd0-118">Parámetros de método comprobados, trabajo iniciado.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="b9dd0-119"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="b9dd0-120">Failed.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b9dd0-121"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="b9dd0-122">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="b9dd0-123"><dt>**No compatible**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="b9dd0-124">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="b9dd0-125">El <dt>**Estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="b9dd0-126">Se desconoce el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="b9dd0-127"><dt>**Tiempo de espera**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="b9dd0-128">Tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="b9dd0-129"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="b9dd0-130">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="b9dd0-131">El <dt>**sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="b9dd0-132">El sistema está en uso.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="b9dd0-133"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="b9dd0-134">Estado no válido para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="b9dd0-135"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="b9dd0-136">Tipo de datos incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="b9dd0-137">El <dt>**sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="b9dd0-138">El sistema no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b9dd0-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="b9dd0-139"><dt>**Memoria**</dt> insuficiente <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="b9dd0-140">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b9dd0-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="b9dd0-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9dd0-141">Requirements</span></span>



| <span data-ttu-id="b9dd0-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9dd0-142">Requirement</span></span> | <span data-ttu-id="b9dd0-143">Value</span><span class="sxs-lookup"><span data-stu-id="b9dd0-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9dd0-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9dd0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b9dd0-145">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9dd0-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9dd0-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9dd0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b9dd0-147">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9dd0-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9dd0-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9dd0-148">Namespace</span></span><br/>                | <span data-ttu-id="b9dd0-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b9dd0-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9dd0-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b9dd0-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9dd0-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9dd0-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9dd0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9dd0-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9dd0-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9dd0-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9dd0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9dd0-155">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="b9dd0-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

