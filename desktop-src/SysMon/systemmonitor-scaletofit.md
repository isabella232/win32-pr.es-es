---
title: SystemMonitor. ScaleToFit, método
description: Ajustar los valores del contador para que quepan en el gráfico.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Método ScaleToFit SysMon
- Método ScaleToFit SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801982"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="4354e-106">SystemMonitor. ScaleToFit, método</span><span class="sxs-lookup"><span data-stu-id="4354e-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="4354e-107">Ajustar los valores del contador para que quepan en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="4354e-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="4354e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4354e-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="4354e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4354e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4354e-110">*selectedCountersOnly* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4354e-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4354e-111">True para escalar solo los contadores seleccionados; de lo contrario, false para escalar todos los contadores.</span><span class="sxs-lookup"><span data-stu-id="4354e-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4354e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4354e-112">Return value</span></span>

<span data-ttu-id="4354e-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4354e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4354e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4354e-114">Remarks</span></span>

<span data-ttu-id="4354e-115">Este método borrará la vista del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4354e-115">This method will clear the graph view.</span></span> <span data-ttu-id="4354e-116">SYSMON usa el factor de escala especificado para cada contador para volver a dibujar el gráfico si el origen de datos es un archivo de registro o empezar a representar gráficamente nuevos valores de contador si el origen de datos es una actividad en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="4354e-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="4354e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4354e-117">Requirements</span></span>



| <span data-ttu-id="4354e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4354e-118">Requirement</span></span> | <span data-ttu-id="4354e-119">Value</span><span class="sxs-lookup"><span data-stu-id="4354e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4354e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4354e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4354e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4354e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4354e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4354e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4354e-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4354e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4354e-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4354e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4354e-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4354e-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4354e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4354e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4354e-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="4354e-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="4354e-128">**Elemento de ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="4354e-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="4354e-129">**Contraelemento. seleccionado**</span><span class="sxs-lookup"><span data-stu-id="4354e-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





