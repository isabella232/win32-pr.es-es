---
description: 'Método ModifyServiceSettings de la Msvm_MetricService clase : modifica los datos de configuración del servicio.'
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings de la Msvm_MetricService clase
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
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112183"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="94da8-103">Método ModifyServiceSettings de la clase \_ MetricService de Msvm</span><span class="sxs-lookup"><span data-stu-id="94da8-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="94da8-104">Modifica los datos de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="94da8-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="94da8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94da8-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="94da8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94da8-107">*SettingData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="94da8-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94da8-108">Contiene una instancia incrustada de la clase [**\_ Msvm MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.</span><span class="sxs-lookup"><span data-stu-id="94da8-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="94da8-109">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="94da8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94da8-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94da8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94da8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94da8-111">Return value</span></span>

<span data-ttu-id="94da8-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="94da8-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="94da8-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94da8-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="94da8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="94da8-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="94da8-115"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="94da8-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="94da8-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="94da8-117"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="94da8-118">Parámetros de método activados, trabajo iniciado.</span><span class="sxs-lookup"><span data-stu-id="94da8-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="94da8-119"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="94da8-120">Failed.</span><span class="sxs-lookup"><span data-stu-id="94da8-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="94da8-121"><dt>**Acceso denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="94da8-122">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="94da8-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="94da8-123"><dt>**No compatible**</dt> <dt>con 32770</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="94da8-124">No compatible.</span><span class="sxs-lookup"><span data-stu-id="94da8-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="94da8-125"><dt>**El estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="94da8-126">Se desconoce el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="94da8-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="94da8-127"><dt>**Tiempo de**</dt> <dt>espera 32772</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="94da8-128">Tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="94da8-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="94da8-129"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="94da8-130">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="94da8-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="94da8-131"><dt>**El sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="94da8-132">El sistema está en uso.</span><span class="sxs-lookup"><span data-stu-id="94da8-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="94da8-133"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="94da8-134">Estado no válido para esta operación.</span><span class="sxs-lookup"><span data-stu-id="94da8-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="94da8-135"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="94da8-136">Tipo de datos incorrecto.</span><span class="sxs-lookup"><span data-stu-id="94da8-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="94da8-137"><dt>**El sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="94da8-138">El sistema no está disponible.</span><span class="sxs-lookup"><span data-stu-id="94da8-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="94da8-139"><dt>**Memoria sin memoria**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="94da8-140">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="94da8-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="94da8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94da8-141">Requirements</span></span>



| <span data-ttu-id="94da8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="94da8-142">Requirement</span></span> | <span data-ttu-id="94da8-143">Valor</span><span class="sxs-lookup"><span data-stu-id="94da8-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94da8-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94da8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="94da8-145">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="94da8-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94da8-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94da8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="94da8-147">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="94da8-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94da8-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94da8-148">Namespace</span></span><br/>                | <span data-ttu-id="94da8-149">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="94da8-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94da8-150">MOF</span><span class="sxs-lookup"><span data-stu-id="94da8-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94da8-151"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94da8-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94da8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94da8-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94da8-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94da8-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94da8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94da8-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="94da8-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

