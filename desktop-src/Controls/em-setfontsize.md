---
title: Mensaje EM_SETFONTSIZE (RichEdit. h)
description: Establece el tamaño de fuente para el texto seleccionado en un control Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490721"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="9e742-104">\_Mensaje SETFONTSIZE em</span><span class="sxs-lookup"><span data-stu-id="9e742-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="9e742-105">Establece el tamaño de fuente para el texto seleccionado en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9e742-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e742-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e742-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e742-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e742-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e742-108">Cambiar el tamaño en puntos del texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9e742-108">Change in point size of the selected text.</span></span> <span data-ttu-id="9e742-109">El resultado se redondeará según los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e742-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="9e742-110">Este parámetro debe estar en el intervalo de-1637 a 1638.</span><span class="sxs-lookup"><span data-stu-id="9e742-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="9e742-111">El tamaño de fuente resultante estará en el intervalo comprendido entre 1 y 1638.</span><span class="sxs-lookup"><span data-stu-id="9e742-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="9e742-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e742-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e742-113">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e742-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e742-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e742-114">Return value</span></span>

<span data-ttu-id="9e742-115">Si no se ha producido ningún error, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="9e742-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="9e742-116">Si se produjo un error, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="9e742-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e742-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e742-117">Remarks</span></span>

<span data-ttu-id="9e742-118">Puede obtener fácilmente el tamaño de fuente enviando el mensaje [**\_ GETCHARFORMAT em**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="9e742-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="9e742-119">La edición enriquecida primero agrega *wParam* al tamaño de fuente actual y, a continuación, usa el tamaño resultante y la tabla siguiente para determinar el valor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="9e742-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="9e742-120">Colores</span><span class="sxs-lookup"><span data-stu-id="9e742-120">Band</span></span>    | <span data-ttu-id="9e742-121">Valor de redondeo</span><span class="sxs-lookup"><span data-stu-id="9e742-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="9e742-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="9e742-122"><=12</span></span> | <span data-ttu-id="9e742-123">1</span><span class="sxs-lookup"><span data-stu-id="9e742-123">1</span></span>              |
| <span data-ttu-id="9e742-124">28</span><span class="sxs-lookup"><span data-stu-id="9e742-124">28</span></span>      | <span data-ttu-id="9e742-125">2</span><span class="sxs-lookup"><span data-stu-id="9e742-125">2</span></span>              |
| <span data-ttu-id="9e742-126">36</span><span class="sxs-lookup"><span data-stu-id="9e742-126">36</span></span>      | <span data-ttu-id="9e742-127">0</span><span class="sxs-lookup"><span data-stu-id="9e742-127">0</span></span>              |
| <span data-ttu-id="9e742-128">48</span><span class="sxs-lookup"><span data-stu-id="9e742-128">48</span></span>      | <span data-ttu-id="9e742-129">0</span><span class="sxs-lookup"><span data-stu-id="9e742-129">0</span></span>              |
| <span data-ttu-id="9e742-130">72</span><span class="sxs-lookup"><span data-stu-id="9e742-130">72</span></span>      | <span data-ttu-id="9e742-131">0</span><span class="sxs-lookup"><span data-stu-id="9e742-131">0</span></span>              |
| <span data-ttu-id="9e742-132">80</span><span class="sxs-lookup"><span data-stu-id="9e742-132">80</span></span>      | <span data-ttu-id="9e742-133">0</span><span class="sxs-lookup"><span data-stu-id="9e742-133">0</span></span>              |
| <span data-ttu-id="9e742-134">> 80</span><span class="sxs-lookup"><span data-stu-id="9e742-134">> 80</span></span> | <span data-ttu-id="9e742-135">10</span><span class="sxs-lookup"><span data-stu-id="9e742-135">10</span></span>             |



 

<span data-ttu-id="9e742-136">Si el tamaño de fuente resultante no es divisible de forma uniforme por el valor de redondeo, el tamaño de fuente se redondea a continuación a un número divisible por el valor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="9e742-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="9e742-137">Por tanto, si el tamaño de fuente es menor o igual que 12, el valor de redondeo será 1.</span><span class="sxs-lookup"><span data-stu-id="9e742-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="9e742-138">Del mismo modo, si el tamaño de fuente es menor o igual que 28, el valor de redondeo es 2.</span><span class="sxs-lookup"><span data-stu-id="9e742-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="9e742-139">En el caso de valores mayores que 28, los tamaños de fuente se redondean a la siguiente banda.</span><span class="sxs-lookup"><span data-stu-id="9e742-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="9e742-140">Por lo tanto, el tamaño de fuente salta a 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="9e742-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="9e742-141">Después 80, todo el redondeo se realiza en incrementos de diez puntos.</span><span class="sxs-lookup"><span data-stu-id="9e742-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="9e742-142">El tamaño de fuente se redondea o reduce verticalmente en función del signo de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="9e742-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="9e742-143">Si *wParam* es positivo, el redondeo siempre estará activo.</span><span class="sxs-lookup"><span data-stu-id="9e742-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="9e742-144">De lo contrario, el redondeo siempre está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9e742-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="9e742-145">Por lo tanto, si el tamaño de fuente actual es 10 y *wParam* es 3, el tamaño de fuente resultante sería 14 (10 + 3 = 13, que no es divisible por 2, por lo que el tamaño se redondea hasta 14).</span><span class="sxs-lookup"><span data-stu-id="9e742-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="9e742-146">Por el contrario, si el tamaño de fuente actual es 14 y *wParam* es-3, el tamaño de fuente resultante sería 10 (14-3 = 11, que no es divisible en 2, por lo que el tamaño se redondea a 10).</span><span class="sxs-lookup"><span data-stu-id="9e742-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="9e742-147">El cambio se aplica a cada parte de la selección.</span><span class="sxs-lookup"><span data-stu-id="9e742-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="9e742-148">Por lo tanto, si parte del texto es 10 PTO y algún 20 PT, después de una llamada con *wParam* establecida en 1, los tamaños de fuente se convierten en 11pt y 22pt, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e742-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="9e742-149">En la tabla siguiente se muestran ejemplos adicionales.</span><span class="sxs-lookup"><span data-stu-id="9e742-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="9e742-150">Tamaño de fuente original</span><span class="sxs-lookup"><span data-stu-id="9e742-150">Original font size</span></span> | <span data-ttu-id="9e742-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e742-151">*wParam*</span></span> | <span data-ttu-id="9e742-152">Tamaño de fuente resultante</span><span class="sxs-lookup"><span data-stu-id="9e742-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="9e742-153">7</span><span class="sxs-lookup"><span data-stu-id="9e742-153">7</span></span>                  | <span data-ttu-id="9e742-154">1</span><span class="sxs-lookup"><span data-stu-id="9e742-154">1</span></span>        | <span data-ttu-id="9e742-155">8</span><span class="sxs-lookup"><span data-stu-id="9e742-155">8</span></span>                   |
| <span data-ttu-id="9e742-156">7</span><span class="sxs-lookup"><span data-stu-id="9e742-156">7</span></span>                  | <span data-ttu-id="9e742-157">3</span><span class="sxs-lookup"><span data-stu-id="9e742-157">3</span></span>        | <span data-ttu-id="9e742-158">10</span><span class="sxs-lookup"><span data-stu-id="9e742-158">10</span></span>                  |
| <span data-ttu-id="9e742-159">10</span><span class="sxs-lookup"><span data-stu-id="9e742-159">10</span></span>                 | <span data-ttu-id="9e742-160">3</span><span class="sxs-lookup"><span data-stu-id="9e742-160">3</span></span>        | <span data-ttu-id="9e742-161">14</span><span class="sxs-lookup"><span data-stu-id="9e742-161">14</span></span>                  |
| <span data-ttu-id="9e742-162">14</span><span class="sxs-lookup"><span data-stu-id="9e742-162">14</span></span>                 | <span data-ttu-id="9e742-163">-3</span><span class="sxs-lookup"><span data-stu-id="9e742-163">-3</span></span>       | <span data-ttu-id="9e742-164">10</span><span class="sxs-lookup"><span data-stu-id="9e742-164">10</span></span>                  |
| <span data-ttu-id="9e742-165">28</span><span class="sxs-lookup"><span data-stu-id="9e742-165">28</span></span>                 | <span data-ttu-id="9e742-166">1</span><span class="sxs-lookup"><span data-stu-id="9e742-166">1</span></span>        | <span data-ttu-id="9e742-167">36</span><span class="sxs-lookup"><span data-stu-id="9e742-167">36</span></span>                  |
| <span data-ttu-id="9e742-168">28</span><span class="sxs-lookup"><span data-stu-id="9e742-168">28</span></span>                 | <span data-ttu-id="9e742-169">3</span><span class="sxs-lookup"><span data-stu-id="9e742-169">3</span></span>        | <span data-ttu-id="9e742-170">36</span><span class="sxs-lookup"><span data-stu-id="9e742-170">36</span></span>                  |
| <span data-ttu-id="9e742-171">80</span><span class="sxs-lookup"><span data-stu-id="9e742-171">80</span></span>                 | <span data-ttu-id="9e742-172">1</span><span class="sxs-lookup"><span data-stu-id="9e742-172">1</span></span>        | <span data-ttu-id="9e742-173">90</span><span class="sxs-lookup"><span data-stu-id="9e742-173">90</span></span>                  |
| <span data-ttu-id="9e742-174">80</span><span class="sxs-lookup"><span data-stu-id="9e742-174">80</span></span>                 | <span data-ttu-id="9e742-175">-1</span><span class="sxs-lookup"><span data-stu-id="9e742-175">-1</span></span>       | <span data-ttu-id="9e742-176">72</span><span class="sxs-lookup"><span data-stu-id="9e742-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="9e742-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e742-177">Requirements</span></span>



| <span data-ttu-id="9e742-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e742-178">Requirement</span></span> | <span data-ttu-id="9e742-179">Value</span><span class="sxs-lookup"><span data-stu-id="9e742-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e742-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e742-180">Minimum supported client</span></span><br/> | <span data-ttu-id="9e742-181">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e742-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e742-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e742-182">Minimum supported server</span></span><br/> | <span data-ttu-id="9e742-183">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e742-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e742-184">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9e742-184">Redistributable</span></span><br/>          | <span data-ttu-id="9e742-185">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="9e742-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="9e742-186">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e742-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e742-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e742-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e742-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e742-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e742-189">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9e742-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e742-190">**\_GETCHARFORMAT em**</span><span class="sxs-lookup"><span data-stu-id="9e742-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="9e742-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="9e742-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="9e742-192">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9e742-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e742-193">Acerca de los controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9e742-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





