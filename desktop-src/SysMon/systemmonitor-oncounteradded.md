---
title: Evento SystemMonitor. OnCounterAdded
description: Le informa cuando un contador se agrega a la colección de contadores.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Evento OnCounterAdded SysMon
- Evento OnCounterAdded SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnCounterAdded
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665982"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="1f7de-106">Evento SystemMonitor. OnCounterAdded</span><span class="sxs-lookup"><span data-stu-id="1f7de-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="1f7de-107">Le informa cuando un contador se agrega a la colección de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7de-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f7de-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="1f7de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f7de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f7de-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1f7de-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f7de-111">Índice del contador agregado al objeto de colección [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7de-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f7de-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f7de-112">Return value</span></span>

<span data-ttu-id="1f7de-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1f7de-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f7de-114">Requirements</span></span>



| <span data-ttu-id="1f7de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7de-115">Requirement</span></span> | <span data-ttu-id="1f7de-116">Value</span><span class="sxs-lookup"><span data-stu-id="1f7de-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7de-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f7de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7de-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1f7de-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1f7de-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f7de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7de-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f7de-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f7de-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f7de-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f7de-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1f7de-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7de-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f7de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7de-124">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="1f7de-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="1f7de-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="1f7de-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





