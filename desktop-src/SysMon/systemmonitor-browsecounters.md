---
title: SystemMonitor BrowseCounters, método
description: Muestra el cuadro de diálogo Agregar contadores.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Método BrowseCounters SysMon
- Método BrowseCounters SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, método BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078828"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="55e42-106">SystemMonitor:: BrowseCounters (método)</span><span class="sxs-lookup"><span data-stu-id="55e42-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="55e42-107">Muestra el cuadro de diálogo **Agregar contadores** .</span><span class="sxs-lookup"><span data-stu-id="55e42-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e42-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55e42-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="55e42-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55e42-109">Parameters</span></span>

<span data-ttu-id="55e42-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="55e42-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55e42-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55e42-111">Return value</span></span>

<span data-ttu-id="55e42-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="55e42-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e42-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55e42-113">Remarks</span></span>

<span data-ttu-id="55e42-114">Este cuadro de diálogo permite al usuario seleccionar contadores de rendimiento locales o remotos en una lista de objetos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="55e42-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="55e42-115">Los contadores seleccionados se agregan a la colección de [**contadores**](counters.md) y se muestran en el gráfico o el informe.</span><span class="sxs-lookup"><span data-stu-id="55e42-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="55e42-116">Para recibir una notificación cuando se agrega un contador, implemente el evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="55e42-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e42-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55e42-117">Requirements</span></span>



| <span data-ttu-id="55e42-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55e42-118">Requirement</span></span> | <span data-ttu-id="55e42-119">Value</span><span class="sxs-lookup"><span data-stu-id="55e42-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e42-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55e42-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55e42-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55e42-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="55e42-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55e42-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55e42-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55e42-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55e42-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55e42-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55e42-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="55e42-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e42-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="55e42-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e42-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="55e42-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="55e42-128">**Counters. Add**</span><span class="sxs-lookup"><span data-stu-id="55e42-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





