---
title: SystemMonitor. SetLogViewRange, método
description: Establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Método SetLogViewRange SysMon
- Método SetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422104"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="6f9fb-106">SystemMonitor. SetLogViewRange, método</span><span class="sxs-lookup"><span data-stu-id="6f9fb-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="6f9fb-107">Establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9fb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9fb-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="6f9fb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9fb-110">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9fb-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9fb-111">Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="6f9fb-112">*StopTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9fb-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9fb-113">Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9fb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9fb-114">Return value</span></span>

<span data-ttu-id="6f9fb-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9fb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f9fb-116">Remarks</span></span>

<span data-ttu-id="6f9fb-117">SYSMON recupera los valores de los contadores de los archivos de registro que se encuentran dentro de las fechas de inicio y de finalización, en su interior.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="6f9fb-118">Si no especifica una fecha de inicio o establece la fecha de inicio en un valor de fecha que está fuera del intervalo de valores de fecha que se encuentra en los archivos de registro, SYSMON cambia el valor al valor de fecha más antiguo que se encuentra en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="6f9fb-119">Si el valor inicial es mayor que el valor de detención, SYSMON cambia el valor inicial para que tenga el mismo valor que el valor de detención.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="6f9fb-120">Si no especifica un valor de detención o establece el valor de detención en un valor de fecha posterior a la última fecha incluida en el archivo de registro, SYSMON cambia el valor al valor de fecha más reciente que se encuentra en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="6f9fb-121">Si el valor de detención es menor que el valor de detención, SYSMON cambia el valor de detención para que tenga el mismo valor que el valor de inicio.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="6f9fb-122">Si especifica una fecha de inicio y de finalización, debe especificar las fechas antes de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="6f9fb-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="6f9fb-123">Si establece las fechas después de establecer **SystemMonitor. DataSourceType**, solo el primer valor de contador se recupera del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="6f9fb-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9fb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f9fb-124">Requirements</span></span>



| <span data-ttu-id="6f9fb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9fb-125">Requirement</span></span> | <span data-ttu-id="6f9fb-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f9fb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9fb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9fb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f9fb-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f9fb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f9fb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9fb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f9fb-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f9fb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f9fb-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f9fb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f9fb-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6f9fb-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9fb-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9fb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9fb-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6f9fb-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="6f9fb-135">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="6f9fb-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





