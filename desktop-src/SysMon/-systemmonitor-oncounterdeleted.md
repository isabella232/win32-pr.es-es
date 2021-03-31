---
title: Evento SystemMonitor. OnCounterDeleted
description: Le notifica antes de que se elimine un contador de la colección de contadores.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Evento OnCounterDeleted SysMon
- Evento OnCounterDeleted SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996445"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="c76fb-106">Evento SystemMonitor. OnCounterDeleted</span><span class="sxs-lookup"><span data-stu-id="c76fb-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="c76fb-107">Le notifica antes de que se elimine un contador de la colección de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="c76fb-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76fb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c76fb-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="c76fb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c76fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76fb-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c76fb-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76fb-111">Índice del contador que se va a eliminar del objeto de colección [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="c76fb-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76fb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c76fb-112">Return value</span></span>

<span data-ttu-id="c76fb-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c76fb-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76fb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c76fb-114">Requirements</span></span>



| <span data-ttu-id="c76fb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76fb-115">Requirement</span></span> | <span data-ttu-id="c76fb-116">Value</span><span class="sxs-lookup"><span data-stu-id="c76fb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c76fb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c76fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c76fb-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c76fb-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c76fb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c76fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c76fb-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c76fb-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c76fb-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c76fb-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c76fb-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c76fb-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76fb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c76fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76fb-124">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="c76fb-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="c76fb-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="c76fb-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





