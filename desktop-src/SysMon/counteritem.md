---
title: Objeto de contraelemento (Isysmon. h)
description: Utilice esta clase para recuperar la ruta de acceso y el valor de un contador y para especificar el color que se usa para representar el contador. Para recuperar este objeto, llame a Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Objeto de contraelemento SysMon
- Objeto de contraelemento SysMon, descrito
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802587"
---
# <a name="counteritem-object"></a><span data-ttu-id="cff7d-106">Objeto de elemento</span><span class="sxs-lookup"><span data-stu-id="cff7d-106">CounterItem object</span></span>

<span data-ttu-id="cff7d-107">Utilice esta clase para recuperar la ruta de acceso y el valor de un contador y para especificar el color que se usa para representar el contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="cff7d-108">Para recuperar este objeto, llame a [**Counters. Item**](counters-item.md).</span><span class="sxs-lookup"><span data-stu-id="cff7d-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="cff7d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cff7d-109">Members</span></span>

<span data-ttu-id="cff7d-110">El objeto de tipo de **elemento** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cff7d-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="cff7d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cff7d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cff7d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cff7d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cff7d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cff7d-113">Methods</span></span>

<span data-ttu-id="cff7d-114">El objeto de **peritem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cff7d-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="cff7d-115">Método</span><span class="sxs-lookup"><span data-stu-id="cff7d-115">Method</span></span>                                             | <span data-ttu-id="cff7d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cff7d-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="cff7d-117">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="cff7d-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="cff7d-118">Recupera los datos del contador de un punto concreto del gráfico de líneas.</span><span class="sxs-lookup"><span data-stu-id="cff7d-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="cff7d-119">**GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="cff7d-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="cff7d-120">Recupera los valores promedio, máximo y mínimo del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="cff7d-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="cff7d-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="cff7d-122">Recupera el último valor del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="cff7d-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cff7d-123">Properties</span></span>

<span data-ttu-id="cff7d-124">El objeto de **peritem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cff7d-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="cff7d-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cff7d-125">Property</span></span>                                                  | <span data-ttu-id="cff7d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="cff7d-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="cff7d-127">**Color**</span><span class="sxs-lookup"><span data-stu-id="cff7d-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="cff7d-128">Recupera o establece el color utilizado para representar el valor del contador en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="cff7d-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="cff7d-129">**Estilo de línea**</span><span class="sxs-lookup"><span data-stu-id="cff7d-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="cff7d-130">Recupera o establece el estilo de línea que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="cff7d-131">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="cff7d-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="cff7d-132">Recupera la ruta de acceso del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="cff7d-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="cff7d-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="cff7d-134">Recupera o establece el factor de escala que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="cff7d-135">**Seleccionado**</span><span class="sxs-lookup"><span data-stu-id="cff7d-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="cff7d-136">Recupera o establece un valor que indica si el contador está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cff7d-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="cff7d-137">**Value**</span><span class="sxs-lookup"><span data-stu-id="cff7d-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="cff7d-138">Recupera el valor actual del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="cff7d-139">**Visible**</span><span class="sxs-lookup"><span data-stu-id="cff7d-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="cff7d-140">Recupera o establece un valor que indica si el contador está gráfico.</span><span class="sxs-lookup"><span data-stu-id="cff7d-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="cff7d-141">**Width**</span><span class="sxs-lookup"><span data-stu-id="cff7d-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="cff7d-142">Recupera o establece el ancho de línea que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="cff7d-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="cff7d-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cff7d-143">Remarks</span></span>

<span data-ttu-id="cff7d-144">[**Value**](counteritem-value.md) es la propiedad predeterminada de **peritem**.</span><span class="sxs-lookup"><span data-stu-id="cff7d-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff7d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cff7d-145">Requirements</span></span>



| <span data-ttu-id="cff7d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cff7d-146">Requirement</span></span> | <span data-ttu-id="cff7d-147">Value</span><span class="sxs-lookup"><span data-stu-id="cff7d-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cff7d-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cff7d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cff7d-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cff7d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cff7d-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cff7d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cff7d-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cff7d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cff7d-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cff7d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff7d-153"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cff7d-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cff7d-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cff7d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff7d-155"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cff7d-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cff7d-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="cff7d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff7d-157">Clases SYSMON</span><span class="sxs-lookup"><span data-stu-id="cff7d-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





