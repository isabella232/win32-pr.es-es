---
title: Evento SystemMonitor. OnDblClick
description: Le informa cuando un usuario hace doble clic en la línea del gráfico, en la barra de histograma o en el elemento de informe con el botón primario del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento de OnDblClick SysMon
- Evento Alhacerdobleclic SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnDblClick
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150338"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="974f9-106">Evento SystemMonitor. OnDblClick</span><span class="sxs-lookup"><span data-stu-id="974f9-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="974f9-107">Le informa cuando un usuario hace doble clic en la línea del gráfico, en la barra de histograma o en el elemento de informe con el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="974f9-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="974f9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="974f9-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="974f9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="974f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974f9-110">*Índice* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="974f9-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="974f9-111">Índice del contador seleccionado en el objeto de colección [**counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="974f9-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="974f9-112">Se devuelve un valor de índice de 0 si no se ha seleccionado ningún contador; de lo contrario, se devuelve el índice del contador seleccionado.</span><span class="sxs-lookup"><span data-stu-id="974f9-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974f9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="974f9-113">Return value</span></span>

<span data-ttu-id="974f9-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="974f9-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="974f9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="974f9-115">Remarks</span></span>

<span data-ttu-id="974f9-116">Cuando se desencadena este evento, el contador que el usuario seleccionó en el gráfico de líneas y el histograma también se selecciona en el panel leyenda.</span><span class="sxs-lookup"><span data-stu-id="974f9-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="974f9-117">Esto hace que sea más fácil para el usuario del monitor de sistema ver qué contador está seleccionado cuando se muestran varios valores de contador.</span><span class="sxs-lookup"><span data-stu-id="974f9-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="974f9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="974f9-118">Requirements</span></span>



| <span data-ttu-id="974f9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="974f9-119">Requirement</span></span> | <span data-ttu-id="974f9-120">Value</span><span class="sxs-lookup"><span data-stu-id="974f9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="974f9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="974f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="974f9-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="974f9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="974f9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="974f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="974f9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="974f9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="974f9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="974f9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="974f9-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="974f9-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





