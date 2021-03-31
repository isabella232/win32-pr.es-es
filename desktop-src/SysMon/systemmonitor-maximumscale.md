---
title: SystemMonitor. MaximumScale (propiedad)
description: Recupera o establece el valor máximo del eje vertical (Y) del gráfico.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propiedad MaximumScale SysMon
- Propiedad MaximumScale SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996259"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="eccc7-106">SystemMonitor. MaximumScale (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eccc7-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="eccc7-107">Recupera o establece el valor máximo del eje vertical (Y) del gráfico.</span><span class="sxs-lookup"><span data-stu-id="eccc7-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="eccc7-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eccc7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccc7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eccc7-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="eccc7-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eccc7-110">Property value</span></span>

<span data-ttu-id="eccc7-111">Valor máximo positivo del eje vertical del gráfico.</span><span class="sxs-lookup"><span data-stu-id="eccc7-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="eccc7-112">El valor máximo predeterminado de la escala vertical es 100.</span><span class="sxs-lookup"><span data-stu-id="eccc7-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="eccc7-113">El valor más bajo en el que se puede establecer el valor máximo es uno más que el valor de [**MinimumScale**](systemmonitor-minimumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="eccc7-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="eccc7-114">El valor más alto en el que puede establecer el valor máximo es 999.999.999.</span><span class="sxs-lookup"><span data-stu-id="eccc7-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="eccc7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eccc7-115">Remarks</span></span>

<span data-ttu-id="eccc7-116">El control ajusta automáticamente la posición de los números de escala que se muestran en la escala vertical según el tamaño del control mostrado.</span><span class="sxs-lookup"><span data-stu-id="eccc7-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccc7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eccc7-117">Requirements</span></span>



| <span data-ttu-id="eccc7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eccc7-118">Requirement</span></span> | <span data-ttu-id="eccc7-119">Value</span><span class="sxs-lookup"><span data-stu-id="eccc7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eccc7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eccc7-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eccc7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eccc7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eccc7-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eccc7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eccc7-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eccc7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eccc7-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="eccc7-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eccc7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="eccc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccc7-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="eccc7-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="eccc7-128">**SystemMonitor. MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="eccc7-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="eccc7-129">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="eccc7-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





