---
title: Counters. Remove (método)
description: Quita una instancia de un objeto de la colección.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Quitar método SysMon
- Remove (método) SysMon, counters (clase)
- Counters (clase) SysMon, Remove (método)
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996261"
---
# <a name="countersremove-method"></a><span data-ttu-id="ac2dc-106">Counters. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="ac2dc-106">Counters.Remove method</span></span>

<span data-ttu-id="ac2dc-107">Quita una instancia de un [**objeto**](counteritem.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac2dc-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="ac2dc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac2dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac2dc-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ac2dc-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac2dc-111">Índice del objeto de [**elemento**](counteritem.md) que se va a quitar de la colección.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="ac2dc-112">El índice está basado en uno.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac2dc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac2dc-113">Return value</span></span>

<span data-ttu-id="ac2dc-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="ac2dc-115">Excepciones</span><span class="sxs-lookup"><span data-stu-id="ac2dc-115">Exceptions</span></span>



| <span data-ttu-id="ac2dc-116">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="ac2dc-116">Exception type</span></span>                                  | <span data-ttu-id="ac2dc-117">Condición</span><span class="sxs-lookup"><span data-stu-id="ac2dc-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ac2dc-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="ac2dc-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="ac2dc-119">El índice especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-119">The specified index is not valid.</span></span> <span data-ttu-id="ac2dc-120">El valor de Err. number es???.</span><span class="sxs-lookup"><span data-stu-id="ac2dc-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ac2dc-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac2dc-121">Remarks</span></span>

<span data-ttu-id="ac2dc-122">Para quitar todos los contadores de la colección, puede llamar a [**SystemMonitor. Reset**](systemmonitor-reset.md).</span><span class="sxs-lookup"><span data-stu-id="ac2dc-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac2dc-123">Requirements</span></span>



| <span data-ttu-id="ac2dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac2dc-124">Requirement</span></span> | <span data-ttu-id="ac2dc-125">Value</span><span class="sxs-lookup"><span data-stu-id="ac2dc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2dc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac2dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2dc-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac2dc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac2dc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac2dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2dc-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac2dc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac2dc-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac2dc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac2dc-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ac2dc-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac2dc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac2dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2dc-133">**Counters**</span><span class="sxs-lookup"><span data-stu-id="ac2dc-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="ac2dc-134">**SystemMonitor. Reset**</span><span class="sxs-lookup"><span data-stu-id="ac2dc-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





