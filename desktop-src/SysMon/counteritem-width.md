---
title: Propiedad de contraelemento. width
description: Recupera o establece el ancho de línea que se usa para representar el valor del contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propiedad ancho (SysMon)
- Propiedad Width SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802491"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="9714f-106">Propiedad de contraelemento. width</span><span class="sxs-lookup"><span data-stu-id="9714f-106">CounterItem.Width property</span></span>

<span data-ttu-id="9714f-107">Recupera o establece el ancho de línea que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="9714f-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="9714f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9714f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9714f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9714f-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="9714f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9714f-110">Property value</span></span>

<span data-ttu-id="9714f-111">Ancho de línea usado en un gráfico de líneas.</span><span class="sxs-lookup"><span data-stu-id="9714f-111">Line width used in a line graph.</span></span> <span data-ttu-id="9714f-112">Los valores válidos oscilan entre 1 y 3, donde 1 (el valor predeterminado) es el ancho menor.</span><span class="sxs-lookup"><span data-stu-id="9714f-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="9714f-113">**Antes de Windows Vista:** Los valores válidos oscilan entre 1 y 9.</span><span class="sxs-lookup"><span data-stu-id="9714f-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="9714f-114">No use un valor de ancho mayor que 3 si la aplicación se ejecutará en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9714f-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="9714f-115">Excepciones</span><span class="sxs-lookup"><span data-stu-id="9714f-115">Exceptions</span></span>



| <span data-ttu-id="9714f-116">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="9714f-116">Exception type</span></span>               | <span data-ttu-id="9714f-117">Condición</span><span class="sxs-lookup"><span data-stu-id="9714f-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="9714f-118">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="9714f-118">**System.ArgumentException**</span></span> | <span data-ttu-id="9714f-119">El ancho de línea especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="9714f-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9714f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9714f-120">Remarks</span></span>

<span data-ttu-id="9714f-121">El ancho de línea predeterminado para los primeros dieciséis contadores que se agregan es 1.</span><span class="sxs-lookup"><span data-stu-id="9714f-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="9714f-122">El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 17-32) que se agregan es 2.</span><span class="sxs-lookup"><span data-stu-id="9714f-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="9714f-123">El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 33-48) que agregue es 3.</span><span class="sxs-lookup"><span data-stu-id="9714f-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="9714f-124">Después, SYSMON selecciona aleatoriamente el ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="9714f-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="9714f-125">Para obtener más información, vea el [**elemento de peritem. color**](counteritem-color.md).</span><span class="sxs-lookup"><span data-stu-id="9714f-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="9714f-126">Para especificar un [**estilo de línea**](counteritem-linestyle.md) distinto de Solid, el ancho debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="9714f-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="9714f-127">Si especifica un valor mayor que 1 y especifica un estilo de línea no sólida, SYSMON omite el ancho de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="9714f-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="9714f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9714f-128">Requirements</span></span>



| <span data-ttu-id="9714f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9714f-129">Requirement</span></span> | <span data-ttu-id="9714f-130">Value</span><span class="sxs-lookup"><span data-stu-id="9714f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9714f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9714f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9714f-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9714f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9714f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9714f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9714f-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9714f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9714f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9714f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9714f-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9714f-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9714f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9714f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9714f-138">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="9714f-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





