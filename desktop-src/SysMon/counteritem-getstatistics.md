---
title: Método GetStatistics
description: Recupera los valores promedio, máximo y mínimo del contador.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Método GetStatistics SysMon
- Método GetStatistics SysMon, clase de contraelemento
- Clase de contraelemento SysMon, método GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996520"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="9582f-106">Método GetStatistics</span><span class="sxs-lookup"><span data-stu-id="9582f-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="9582f-107">Recupera los valores promedio, máximo y mínimo del contador.</span><span class="sxs-lookup"><span data-stu-id="9582f-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9582f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9582f-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="9582f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9582f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9582f-110">*máx* \[ . enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9582f-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9582f-111">Valor máximo del contador.</span><span class="sxs-lookup"><span data-stu-id="9582f-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="9582f-112">*mín* \[ . enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9582f-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9582f-113">Valor mínimo del contador.</span><span class="sxs-lookup"><span data-stu-id="9582f-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="9582f-114">*promedio* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9582f-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9582f-115">Valor medio del contador.</span><span class="sxs-lookup"><span data-stu-id="9582f-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="9582f-116">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9582f-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9582f-117">Indica si los valores son válidos.</span><span class="sxs-lookup"><span data-stu-id="9582f-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="9582f-118">Value</span><span class="sxs-lookup"><span data-stu-id="9582f-118">Value</span></span>                                                                                              | <span data-ttu-id="9582f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9582f-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="9582f-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9582f-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9582f-121">Los valores son válidos.</span><span class="sxs-lookup"><span data-stu-id="9582f-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="9582f-122"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="9582f-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="9582f-123">Los valores no son válidos.</span><span class="sxs-lookup"><span data-stu-id="9582f-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9582f-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9582f-124">Return value</span></span>

<span data-ttu-id="9582f-125">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9582f-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9582f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9582f-126">Remarks</span></span>

<span data-ttu-id="9582f-127">Solo los valores del contador que se ven en la ventana del gráfico se usan para calcular los valores estadísticos.</span><span class="sxs-lookup"><span data-stu-id="9582f-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9582f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9582f-128">Requirements</span></span>



| <span data-ttu-id="9582f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9582f-129">Requirement</span></span> | <span data-ttu-id="9582f-130">Value</span><span class="sxs-lookup"><span data-stu-id="9582f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9582f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9582f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9582f-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9582f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9582f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9582f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9582f-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9582f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9582f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9582f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9582f-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9582f-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9582f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9582f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9582f-138">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="9582f-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="9582f-139">**Elemento de GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="9582f-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="9582f-140">**Peritem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="9582f-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





