---
title: Propiedad SystemMonitor. UpdateInterval
description: Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propiedad UpdateInterval SysMon
- Propiedad UpdateInterval SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996315"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="8ec24-106">Propiedad SystemMonitor. UpdateInterval</span><span class="sxs-lookup"><span data-stu-id="8ec24-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="8ec24-107">Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe.</span><span class="sxs-lookup"><span data-stu-id="8ec24-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="8ec24-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ec24-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec24-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ec24-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="8ec24-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8ec24-110">Property value</span></span>

<span data-ttu-id="8ec24-111">Período de tiempo, en segundos, que SYSMON espera antes de la próxima vez que recopila datos de contador y actualiza el gráfico o el informe.</span><span class="sxs-lookup"><span data-stu-id="8ec24-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="8ec24-112">El intervalo mínimo es 1 segundo (este también es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="8ec24-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="8ec24-113">El valor máximo es 1 millón.</span><span class="sxs-lookup"><span data-stu-id="8ec24-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ec24-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ec24-114">Remarks</span></span>

<span data-ttu-id="8ec24-115">Esta propiedad solo es relevante cuando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) se establece en false.</span><span class="sxs-lookup"><span data-stu-id="8ec24-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec24-116">Requirements</span></span>



| <span data-ttu-id="8ec24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec24-117">Requirement</span></span> | <span data-ttu-id="8ec24-118">Value</span><span class="sxs-lookup"><span data-stu-id="8ec24-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec24-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec24-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ec24-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8ec24-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec24-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ec24-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ec24-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ec24-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ec24-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8ec24-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec24-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec24-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8ec24-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





