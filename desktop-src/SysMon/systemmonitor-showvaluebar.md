---
title: Propiedad SystemMonitor. ShowValueBar
description: Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos por debajo del gráfico) se muestra en el control.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propiedad ShowValueBar SysMon
- Propiedad ShowValueBar SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801616"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="a3de6-106">Propiedad SystemMonitor. ShowValueBar</span><span class="sxs-lookup"><span data-stu-id="a3de6-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="a3de6-107">Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos por debajo del gráfico) se muestra en el control.</span><span class="sxs-lookup"><span data-stu-id="a3de6-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="a3de6-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a3de6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3de6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3de6-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a3de6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a3de6-110">Property value</span></span>

<span data-ttu-id="a3de6-111">True indica que la barra de valores se muestra en el control; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="a3de6-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="a3de6-112">El valor predeterminado de esta propiedad es true.</span><span class="sxs-lookup"><span data-stu-id="a3de6-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3de6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3de6-113">Remarks</span></span>

<span data-ttu-id="a3de6-114">Las estadísticas mostradas incluyen el último valor, el valor medio y los valores mínimo y máximo del contador seleccionado actualmente en el intervalo de tiempo mostrado.</span><span class="sxs-lookup"><span data-stu-id="a3de6-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="a3de6-115">Para seleccionar los valores del contador que se van a mostrar, el usuario debe seleccionar el contador en el panel leyenda del control.</span><span class="sxs-lookup"><span data-stu-id="a3de6-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3de6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3de6-116">Requirements</span></span>



| <span data-ttu-id="a3de6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3de6-117">Requirement</span></span> | <span data-ttu-id="a3de6-118">Value</span><span class="sxs-lookup"><span data-stu-id="a3de6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3de6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3de6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3de6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3de6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a3de6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3de6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3de6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3de6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3de6-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3de6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3de6-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a3de6-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3de6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3de6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3de6-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="a3de6-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





