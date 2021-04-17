---
description: Permite iniciar la especificación de la recopilación de métricas puntuales y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Método ControlSampleTimes de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687650"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="04366-103">Método ControlSampleTimes de la \_ clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="04366-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="04366-104">Permite iniciar la especificación de la recopilación de métricas puntuales y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.</span><span class="sxs-lookup"><span data-stu-id="04366-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="04366-105">Cada vez que se inicia el muestreo de métricas adicionales, se puede usar la configuración especificada por este método.</span><span class="sxs-lookup"><span data-stu-id="04366-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="04366-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04366-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="04366-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04366-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04366-108">*StartSampleTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04366-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04366-109">Un momento dado en el que se va a iniciar el muestreo de las métricas.</span><span class="sxs-lookup"><span data-stu-id="04366-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="04366-110">Un valor de 99990101000000.000000 + 000 indicará que el muestreo debe iniciarse en la próxima vez que se sincronice con la hora completa.</span><span class="sxs-lookup"><span data-stu-id="04366-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="04366-111">El muestreo se sincroniza con la hora completa si los segundos desde el intervalo de ejemplo de módulo medianoche en segundos es igual a 0.</span><span class="sxs-lookup"><span data-stu-id="04366-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="04366-112">*PreferredSampleInterval* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04366-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04366-113">Tiempo de intervalo de muestra preferido.</span><span class="sxs-lookup"><span data-stu-id="04366-113">Preferred sample interval time.</span></span> <span data-ttu-id="04366-114">Para obtener métricas que se pueden correlacionar, se recomienda elegir el intervalo de ejemplo de modo que el tiempo de intervalo de ejemplo de módulo 3600 en segundos sea igual a 0.</span><span class="sxs-lookup"><span data-stu-id="04366-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="04366-115">Es responsabilidad de la implementación del servicio de métricas de CIM decidir si se respeta el tiempo de intervalo de muestra solicitado.</span><span class="sxs-lookup"><span data-stu-id="04366-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="04366-116">El cliente CIM puede comprobar si los proveedores de métricas respetan el tiempo de intervalo de muestra solicitado recuperando instancias de BaseMetricDefinition relacionadas y comprobando el contenido de la [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md).**Propiedad SampleInterval** .</span><span class="sxs-lookup"><span data-stu-id="04366-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="04366-117">*RestartGathering* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04366-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04366-118">**True** para solicitar que la recopilación de todas las métricas asociadas al servicio de métrica se reinicie con esta llamada al método.</span><span class="sxs-lookup"><span data-stu-id="04366-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04366-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04366-119">Return value</span></span>

<span data-ttu-id="04366-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="04366-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="04366-121">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="04366-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04366-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="04366-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04366-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="04366-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04366-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04366-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04366-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="04366-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="04366-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04366-126">Requirements</span></span>



| <span data-ttu-id="04366-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04366-127">Requirement</span></span> | <span data-ttu-id="04366-128">Value</span><span class="sxs-lookup"><span data-stu-id="04366-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04366-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04366-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04366-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="04366-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="04366-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04366-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04366-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04366-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="04366-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="04366-133">Namespace</span></span><br/>                | <span data-ttu-id="04366-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="04366-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="04366-135">MOF</span><span class="sxs-lookup"><span data-stu-id="04366-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04366-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04366-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04366-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04366-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04366-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04366-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04366-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="04366-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04366-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="04366-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




