---
title: Propiedad SystemMonitor. MinimumScale
description: Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propiedad MinimumScale SysMon
- Propiedad MinimumScale SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490468"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="bc7b4-106">Propiedad SystemMonitor. MinimumScale</span><span class="sxs-lookup"><span data-stu-id="bc7b4-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="bc7b4-107">Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.</span><span class="sxs-lookup"><span data-stu-id="bc7b4-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="bc7b4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bc7b4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc7b4-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="bc7b4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bc7b4-110">Property value</span></span>

<span data-ttu-id="bc7b4-111">Valor mínimo positivo del eje vertical del gráfico.</span><span class="sxs-lookup"><span data-stu-id="bc7b4-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="bc7b4-112">El valor mínimo predeterminado de la escala vertical es 0.</span><span class="sxs-lookup"><span data-stu-id="bc7b4-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="bc7b4-113">El valor más alto en el que se puede establecer el valor mínimo es uno menos que el valor [**MaximumScale**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7b4-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc7b4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc7b4-114">Remarks</span></span>

<span data-ttu-id="bc7b4-115">El control ajusta automáticamente la posición de los números de escala que se muestran en la escala vertical según el tamaño del control mostrado.</span><span class="sxs-lookup"><span data-stu-id="bc7b4-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc7b4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc7b4-116">Requirements</span></span>



| <span data-ttu-id="bc7b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc7b4-117">Requirement</span></span> | <span data-ttu-id="bc7b4-118">Value</span><span class="sxs-lookup"><span data-stu-id="bc7b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7b4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc7b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc7b4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc7b4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bc7b4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc7b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc7b4-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc7b4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc7b4-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc7b4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc7b4-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bc7b4-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc7b4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc7b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc7b4-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="bc7b4-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bc7b4-127">**SystemMonitor. MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="bc7b4-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="bc7b4-128">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="bc7b4-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





