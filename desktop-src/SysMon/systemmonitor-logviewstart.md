---
title: Propiedad SystemMonitor. LogViewStart
description: Recupera o establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propiedad LogViewStart SysMon
- Propiedad LogViewStart SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996260"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="8534e-106">Propiedad SystemMonitor. LogViewStart</span><span class="sxs-lookup"><span data-stu-id="8534e-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="8534e-107">Recupera o establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="8534e-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="8534e-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8534e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8534e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8534e-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="8534e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8534e-110">Property value</span></span>

<span data-ttu-id="8534e-111">Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="8534e-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="8534e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8534e-112">Remarks</span></span>

<span data-ttu-id="8534e-113">SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de las fechas de inicio y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="8534e-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="8534e-114">Si no especifica una fecha de inicio o establece esta propiedad en un valor de fecha que está fuera del intervalo de valores de fecha que se encuentra en los archivos de registro, SYSMON cambia el valor al valor de fecha más antiguo que se encuentra en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="8534e-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="8534e-115">Si esta propiedad se establece en un valor de fecha mayor que [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON cambia el valor al valor de **LogViewStop**.</span><span class="sxs-lookup"><span data-stu-id="8534e-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="8534e-116">Si especifica una fecha de inicio y de finalización, debe especificar las fechas antes de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="8534e-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8534e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8534e-117">Requirements</span></span>



| <span data-ttu-id="8534e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8534e-118">Requirement</span></span> | <span data-ttu-id="8534e-119">Value</span><span class="sxs-lookup"><span data-stu-id="8534e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8534e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8534e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8534e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8534e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8534e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8534e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8534e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8534e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8534e-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8534e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8534e-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8534e-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8534e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8534e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8534e-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8534e-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="8534e-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="8534e-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="8534e-129">**SystemMonitor. logfiles**</span><span class="sxs-lookup"><span data-stu-id="8534e-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="8534e-130">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="8534e-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="8534e-131">**SystemMonitor.LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="8534e-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="8534e-132">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="8534e-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





