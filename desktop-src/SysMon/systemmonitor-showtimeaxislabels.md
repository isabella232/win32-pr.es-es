---
title: Propiedad SystemMonitor. ShowTimeAxisLabels
description: Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propiedad ShowTimeAxisLabels SysMon
- Propiedad ShowTimeAxisLabels SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665941"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="df42d-106">Propiedad SystemMonitor. ShowTimeAxisLabels</span><span class="sxs-lookup"><span data-stu-id="df42d-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="df42d-107">Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.</span><span class="sxs-lookup"><span data-stu-id="df42d-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="df42d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df42d-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="df42d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="df42d-109">Property value</span></span>

<span data-ttu-id="df42d-110">Si el valor es true, se aplicarán etiquetas al eje x.</span><span class="sxs-lookup"><span data-stu-id="df42d-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="df42d-111">Un valor de false no lo será.</span><span class="sxs-lookup"><span data-stu-id="df42d-111">A value of False will not.</span></span> <span data-ttu-id="df42d-112">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="df42d-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="df42d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df42d-113">Remarks</span></span>

<span data-ttu-id="df42d-114">SYSMON omite esta propiedad para los gráficos de barras, informes e histogramas.</span><span class="sxs-lookup"><span data-stu-id="df42d-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="df42d-115">En el caso de los gráficos de líneas, SYSMON usa la hora a la que se muestreó el valor del contador como etiqueta.</span><span class="sxs-lookup"><span data-stu-id="df42d-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="df42d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df42d-116">Requirements</span></span>



| <span data-ttu-id="df42d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df42d-117">Requirement</span></span> | <span data-ttu-id="df42d-118">Value</span><span class="sxs-lookup"><span data-stu-id="df42d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df42d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df42d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df42d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df42d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df42d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df42d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df42d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df42d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df42d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df42d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df42d-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="df42d-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





