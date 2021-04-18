---
title: Propiedad SystemMonitor. EnableToolTips
description: Recupera o establece un valor que determina si se muestra una información sobre herramientas cuando se mantiene el mouse sobre un contador en una de las vistas del gráfico (no se admite para la vista de informe).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propiedad EnableToolTips SysMon
- Propiedad EnableToolTips SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666004"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="9b3f5-106">Propiedad SystemMonitor. EnableToolTips</span><span class="sxs-lookup"><span data-stu-id="9b3f5-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="9b3f5-107">Recupera o establece un valor que determina si se muestra una información sobre herramientas cuando se mantiene el mouse sobre un contador en una de las vistas del gráfico (no se admite para la vista de informe).</span><span class="sxs-lookup"><span data-stu-id="9b3f5-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b3f5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b3f5-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9b3f5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9b3f5-109">Property value</span></span>

<span data-ttu-id="9b3f5-110">True muestra una información sobre herramientas con la información del contador. en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b3f5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b3f5-111">Remarks</span></span>

<span data-ttu-id="9b3f5-112">En el caso de los gráficos de líneas, la información sobre herramientas está delimitada por el punto de datos más cercano al mouse.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="9b3f5-113">En el caso de los gráficos de barras e histogramas, la información sobre herramientas representa el valor de datos total de la barra, no un punto dentro de la barra.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="9b3f5-114">La información sobre herramientas contiene información diferente en función del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="9b3f5-115">En el caso de los archivos de registro, la información sobre herramientas contiene la ruta de acceso del contador, el valor del contador, la marca de tiempo, el número de muestras de datos incluidas en el punto de datos y los valores de datos mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="9b3f5-116">Para la actividad en tiempo real, la información sobre herramientas contiene la ruta de acceso del contador, el valor del contador y la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="9b3f5-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b3f5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b3f5-117">Requirements</span></span>



| <span data-ttu-id="9b3f5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b3f5-118">Requirement</span></span> | <span data-ttu-id="9b3f5-119">Value</span><span class="sxs-lookup"><span data-stu-id="9b3f5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3f5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b3f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b3f5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9b3f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b3f5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b3f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b3f5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b3f5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b3f5-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b3f5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b3f5-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9b3f5-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





