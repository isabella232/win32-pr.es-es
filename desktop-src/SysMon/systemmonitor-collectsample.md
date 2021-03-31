---
title: SystemMonitor CollectSample, método
description: Muestrea un valor para cada contador del objeto Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Método CollectSample SysMon
- Método CollectSample SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, método CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490990"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="8c216-106">SystemMonitor:: CollectSample (método)</span><span class="sxs-lookup"><span data-stu-id="8c216-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="8c216-107">Muestrea un valor para cada contador del objeto [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="8c216-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c216-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c216-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="8c216-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c216-109">Parameters</span></span>

<span data-ttu-id="8c216-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c216-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c216-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c216-111">Return value</span></span>

<span data-ttu-id="8c216-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c216-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c216-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c216-113">Remarks</span></span>

<span data-ttu-id="8c216-114">Llame a **CollectSample** solo si [**ManualUpdate**](systemmonitor-manualupdate.md) es true y va a tomar muestras de los valores de contador de la actividad actual del equipo no usar este método al realizar el muestreo desde un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="8c216-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="8c216-115">El gráfico o informe se actualiza con el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="8c216-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="8c216-116">Tenga en cuenta que algunos tipos de gráficos necesitan dos muestras para representar gráficamente los datos, por ejemplo, el gráfico de líneas.</span><span class="sxs-lookup"><span data-stu-id="8c216-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="8c216-117">Para recibir una notificación cuando se ha recopilado el ejemplo, implemente el evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .</span><span class="sxs-lookup"><span data-stu-id="8c216-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c216-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c216-118">Requirements</span></span>



| <span data-ttu-id="8c216-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c216-119">Requirement</span></span> | <span data-ttu-id="8c216-120">Value</span><span class="sxs-lookup"><span data-stu-id="8c216-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c216-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c216-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c216-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c216-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8c216-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c216-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c216-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c216-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c216-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c216-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c216-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8c216-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c216-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c216-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c216-128">**Counters**</span><span class="sxs-lookup"><span data-stu-id="8c216-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="8c216-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8c216-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





