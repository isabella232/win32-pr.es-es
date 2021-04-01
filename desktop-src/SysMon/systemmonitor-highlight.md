---
title: SystemMonitor. Highlight (propiedad)
description: Recupera o establece un valor que indica si los valores de los contadores seleccionados se resaltan en el gráfico.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Resaltar propiedad SysMon
- Resaltar propiedad SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad Highlight
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905266"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="ffd65-106">SystemMonitor. Highlight (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ffd65-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="ffd65-107">Recupera o establece un valor que indica si los valores de los contadores seleccionados se resaltan en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ffd65-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="ffd65-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffd65-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd65-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffd65-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ffd65-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffd65-110">Property value</span></span>

<span data-ttu-id="ffd65-111">True indica que los valores de los contadores seleccionados se resaltan en el gráfico; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="ffd65-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="ffd65-112">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="ffd65-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd65-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffd65-113">Remarks</span></span>

<span data-ttu-id="ffd65-114">Para seleccionar uno o varios contadores, puede establecer el valor de [**peritem. Selected**](counteritem-selected.md) en true o el usuario puede seleccionar los contadores de la lista de contadores que se muestran en la leyenda.</span><span class="sxs-lookup"><span data-stu-id="ffd65-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="ffd65-115">**Antes de Windows Vista:** No puede seleccionar contadores mediante programación y el usuario puede seleccionar un solo contador de la lista de contadores que se muestra en la leyenda.</span><span class="sxs-lookup"><span data-stu-id="ffd65-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="ffd65-116">El resaltado puede ser negro o blanco, dependiendo del valor de la propiedad [**BackColor**](systemmonitor-backcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd65-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="ffd65-117">El resaltado se establece automáticamente en el color que proporcionará el contraste suficiente entre el color de resaltado y el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="ffd65-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd65-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd65-118">Requirements</span></span>



| <span data-ttu-id="ffd65-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd65-119">Requirement</span></span> | <span data-ttu-id="ffd65-120">Value</span><span class="sxs-lookup"><span data-stu-id="ffd65-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd65-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd65-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd65-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ffd65-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ffd65-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd65-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd65-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffd65-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffd65-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffd65-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd65-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ffd65-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffd65-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffd65-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd65-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ffd65-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="ffd65-129">**Contraelemento. seleccionado**</span><span class="sxs-lookup"><span data-stu-id="ffd65-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





