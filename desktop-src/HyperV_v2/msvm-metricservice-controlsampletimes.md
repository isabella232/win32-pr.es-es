---
description: Establece las horas de muestra del control.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Método ControlSampleTimes de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276732"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="03e8f-103">Método ControlSampleTimes de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="03e8f-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="03e8f-104">Establece las horas de muestra del control.</span><span class="sxs-lookup"><span data-stu-id="03e8f-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03e8f-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="03e8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03e8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03e8f-107">*StartSampleTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03e8f-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03e8f-108">Un momento dado en el que se va a iniciar el muestreo de las métricas.</span><span class="sxs-lookup"><span data-stu-id="03e8f-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="03e8f-109">Un valor de 99990101000000.000000 + 000 indicará que el muestreo debe iniciarse en la próxima vez que se sincronice con la hora completa.</span><span class="sxs-lookup"><span data-stu-id="03e8f-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="03e8f-110">El muestreo se sincroniza con la hora completa si los segundos desde el intervalo de ejemplo de módulo medianoche en segundos es igual a 0.</span><span class="sxs-lookup"><span data-stu-id="03e8f-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="03e8f-111">*PreferredSampleInterval* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03e8f-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03e8f-112">Tiempo de intervalo de muestra preferido.</span><span class="sxs-lookup"><span data-stu-id="03e8f-112">Preferred sample interval time.</span></span> <span data-ttu-id="03e8f-113">Para obtener métricas que se pueden correlacionar, se recomienda elegir el intervalo de ejemplo de modo que el tiempo de intervalo de ejemplo de módulo 3600 en segundos sea igual a 0.</span><span class="sxs-lookup"><span data-stu-id="03e8f-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="03e8f-114">Es responsabilidad de la implementación del servicio de métricas de CIM decidir si se respeta el tiempo de intervalo de muestra solicitado.</span><span class="sxs-lookup"><span data-stu-id="03e8f-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="03e8f-115">El cliente CIM puede comprobar si los proveedores de métricas respetan el tiempo de intervalo de muestra solicitado recuperando instancias de BaseMetricDefinition relacionadas y comprobando el contenido de la \_ propiedad "CIM BaseMetricDefinition. SampleInterval".</span><span class="sxs-lookup"><span data-stu-id="03e8f-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="03e8f-116">*RestartGathering* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03e8f-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03e8f-117">Valor booleano que, cuando se establece en TRUE, solicita que la recopilación de todas las métricas asociadas al servicio de métrica se reinicie con esta llamada al método.</span><span class="sxs-lookup"><span data-stu-id="03e8f-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03e8f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03e8f-118">Return value</span></span>

<span data-ttu-id="03e8f-119">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="03e8f-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="03e8f-120">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="03e8f-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="03e8f-121">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="03e8f-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="03e8f-122">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="03e8f-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="03e8f-123">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="03e8f-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="03e8f-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="03e8f-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="03e8f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03e8f-125">Requirements</span></span>



| <span data-ttu-id="03e8f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e8f-126">Requirement</span></span> | <span data-ttu-id="03e8f-127">Value</span><span class="sxs-lookup"><span data-stu-id="03e8f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e8f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="03e8f-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03e8f-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="03e8f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="03e8f-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="03e8f-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="03e8f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03e8f-132">Namespace</span></span><br/>                | <span data-ttu-id="03e8f-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="03e8f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03e8f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="03e8f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03e8f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03e8f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03e8f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03e8f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03e8f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03e8f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03e8f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e8f-139">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="03e8f-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




