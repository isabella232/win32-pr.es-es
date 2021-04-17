---
title: Propiedad SystemMonitor. ManualUpdate
description: Recupera o establece un valor que indica si el contenido del monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Propiedad ManualUpdate SysMon
- Propiedad ManualUpdate SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665983"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="95a4b-106">Propiedad SystemMonitor. ManualUpdate</span><span class="sxs-lookup"><span data-stu-id="95a4b-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="95a4b-107">Recupera o establece un valor que indica si el contenido del monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="95a4b-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="95a4b-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="95a4b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a4b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95a4b-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="95a4b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="95a4b-110">Property value</span></span>

<span data-ttu-id="95a4b-111">True indica que el gráfico se actualiza manualmente.</span><span class="sxs-lookup"><span data-stu-id="95a4b-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="95a4b-112">False indica que el gráfico se actualiza automáticamente según el intervalo de actualización especificado en [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md).</span><span class="sxs-lookup"><span data-stu-id="95a4b-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95a4b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95a4b-113">Remarks</span></span>

<span data-ttu-id="95a4b-114">De forma predeterminada, el gráfico se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="95a4b-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="95a4b-115">Para actualizar el gráfico manualmente, llame al método [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) .</span><span class="sxs-lookup"><span data-stu-id="95a4b-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a4b-116">Requirements</span></span>



| <span data-ttu-id="95a4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a4b-117">Requirement</span></span> | <span data-ttu-id="95a4b-118">Value</span><span class="sxs-lookup"><span data-stu-id="95a4b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95a4b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95a4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95a4b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95a4b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="95a4b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95a4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95a4b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95a4b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95a4b-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95a4b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95a4b-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="95a4b-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a4b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="95a4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a4b-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="95a4b-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="95a4b-127">**SystemMonitor.CollectSample**</span><span class="sxs-lookup"><span data-stu-id="95a4b-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="95a4b-128">**SystemMonitor.UpdateGraph**</span><span class="sxs-lookup"><span data-stu-id="95a4b-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





