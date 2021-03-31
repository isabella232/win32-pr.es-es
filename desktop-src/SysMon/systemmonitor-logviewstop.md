---
title: Propiedad SystemMonitor. LogViewStop
description: Recupera o establece la fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propiedad LogViewStop SysMon
- Propiedad LogViewStop SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996352"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="7afdd-106">Propiedad SystemMonitor. LogViewStop</span><span class="sxs-lookup"><span data-stu-id="7afdd-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="7afdd-107">Recupera o establece la fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="7afdd-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="7afdd-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7afdd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7afdd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7afdd-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="7afdd-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7afdd-110">Property value</span></span>

<span data-ttu-id="7afdd-111">Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="7afdd-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="7afdd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7afdd-112">Remarks</span></span>

<span data-ttu-id="7afdd-113">SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y las fechas de detención, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="7afdd-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="7afdd-114">Si no especifica un valor de detención o establece esta propiedad en un valor de fecha posterior a la última fecha incluida en el archivo de registro, SYSMON cambia el valor al valor de fecha más reciente que se encuentra en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="7afdd-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="7afdd-115">Si esta propiedad se establece en un valor de fecha menor que [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON cambia el valor al valor de **LogViewStart**.</span><span class="sxs-lookup"><span data-stu-id="7afdd-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="7afdd-116">Debe establecer la fecha de inicio antes de establecer la fecha de detención; de lo contrario, ambos valores se establecen en Date. MinValue y, si establece las fechas después de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md), solo se recupera el primer valor de contador del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="7afdd-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7afdd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7afdd-117">Requirements</span></span>



| <span data-ttu-id="7afdd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7afdd-118">Requirement</span></span> | <span data-ttu-id="7afdd-119">Value</span><span class="sxs-lookup"><span data-stu-id="7afdd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7afdd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7afdd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7afdd-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7afdd-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7afdd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7afdd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7afdd-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7afdd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7afdd-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7afdd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7afdd-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7afdd-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afdd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7afdd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afdd-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="7afdd-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="7afdd-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="7afdd-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="7afdd-129">**SystemMonitor.LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="7afdd-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="7afdd-130">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="7afdd-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="7afdd-131">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="7afdd-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





