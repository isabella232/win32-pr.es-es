---
title: Evento SystemMonitor. OnCounterSelected
description: Le notifica cuando se selecciona un contador.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Evento OnCounterSelected SysMon
- Evento OnCounterSelected SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666006"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="daf25-106">Evento SystemMonitor. OnCounterSelected</span><span class="sxs-lookup"><span data-stu-id="daf25-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="daf25-107">Le notifica cuando se selecciona un contador.</span><span class="sxs-lookup"><span data-stu-id="daf25-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daf25-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="daf25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daf25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf25-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="daf25-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daf25-111">Índice del contador seleccionado en el objeto de colección [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="daf25-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf25-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daf25-112">Return value</span></span>

<span data-ttu-id="daf25-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="daf25-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf25-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daf25-114">Remarks</span></span>

<span data-ttu-id="daf25-115">Puede recibir este evento cuando</span><span class="sxs-lookup"><span data-stu-id="daf25-115">You can receive this event when</span></span>

-   <span data-ttu-id="daf25-116">El valor de el elemento se establece en true [**.**](counteritem-selected.md)</span><span class="sxs-lookup"><span data-stu-id="daf25-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="daf25-117">El usuario selecciona un contador en la leyenda</span><span class="sxs-lookup"><span data-stu-id="daf25-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="daf25-118">El usuario hace doble clic en un contador de la leyenda</span><span class="sxs-lookup"><span data-stu-id="daf25-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="daf25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daf25-119">Requirements</span></span>



| <span data-ttu-id="daf25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf25-120">Requirement</span></span> | <span data-ttu-id="daf25-121">Value</span><span class="sxs-lookup"><span data-stu-id="daf25-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daf25-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daf25-122">Minimum supported client</span></span><br/> | <span data-ttu-id="daf25-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="daf25-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="daf25-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daf25-124">Minimum supported server</span></span><br/> | <span data-ttu-id="daf25-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="daf25-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="daf25-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="daf25-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf25-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="daf25-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf25-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="daf25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf25-129">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="daf25-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="daf25-130">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="daf25-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





