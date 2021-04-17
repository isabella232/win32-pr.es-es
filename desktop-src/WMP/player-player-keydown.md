---
title: Player. KeyDown (evento)
description: El evento KeyDown tiene lugar cuando se presiona una tecla. | Player. KeyDown (evento)
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Media Player de eventos KeyDown de Windows
- Evento KeyDown Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690818"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="b32ce-107">Player. KeyDown (evento)</span><span class="sxs-lookup"><span data-stu-id="b32ce-107">Player.KeyDown event</span></span>

<span data-ttu-id="b32ce-108">El evento **KeyDown** tiene lugar cuando se presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="b32ce-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32ce-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b32ce-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="b32ce-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b32ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32ce-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="b32ce-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b32ce-112">**Número** (**int**) que especifica qué tecla física se presiona.</span><span class="sxs-lookup"><span data-stu-id="b32ce-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="b32ce-113">Para los valores posibles, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b32ce-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b32ce-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="b32ce-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="b32ce-115">**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="b32ce-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="b32ce-116">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b32ce-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="b32ce-117">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="b32ce-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="b32ce-118">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="b32ce-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32ce-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b32ce-119">Return value</span></span>

<span data-ttu-id="b32ce-120">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b32ce-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32ce-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b32ce-121">Remarks</span></span>

<span data-ttu-id="b32ce-122">El argumento *nKeyCode* especifica una clave física.</span><span class="sxs-lookup"><span data-stu-id="b32ce-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="b32ce-123">En las tablas siguientes se muestran los posibles valores de las claves principales de un teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="b32ce-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="b32ce-124">Valores de las claves principales.</span><span class="sxs-lookup"><span data-stu-id="b32ce-124">Values for the main keys.</span></span>



| <span data-ttu-id="b32ce-125">Clave</span><span class="sxs-lookup"><span data-stu-id="b32ce-125">Key</span></span>                     | <span data-ttu-id="b32ce-126">Value</span><span class="sxs-lookup"><span data-stu-id="b32ce-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="b32ce-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="b32ce-127">A-Z</span></span>                     | <span data-ttu-id="b32ce-128">65-90</span><span class="sxs-lookup"><span data-stu-id="b32ce-128">65-90</span></span>   |
| <span data-ttu-id="b32ce-129">0-9</span><span class="sxs-lookup"><span data-stu-id="b32ce-129">0-9</span></span>                     | <span data-ttu-id="b32ce-130">48-56</span><span class="sxs-lookup"><span data-stu-id="b32ce-130">48-56</span></span>   |
| <span data-ttu-id="b32ce-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="b32ce-131">F1-F12</span></span>                  | <span data-ttu-id="b32ce-132">112-123</span><span class="sxs-lookup"><span data-stu-id="b32ce-132">112-123</span></span> |
| <span data-ttu-id="b32ce-133">ESC</span><span class="sxs-lookup"><span data-stu-id="b32ce-133">ESC</span></span>                     | <span data-ttu-id="b32ce-134">27</span><span class="sxs-lookup"><span data-stu-id="b32ce-134">27</span></span>      |
| <span data-ttu-id="b32ce-135">TAB</span><span class="sxs-lookup"><span data-stu-id="b32ce-135">TAB</span></span>                     | <span data-ttu-id="b32ce-136">9</span><span class="sxs-lookup"><span data-stu-id="b32ce-136">9</span></span>       |
| <span data-ttu-id="b32ce-137">Bloq Mayús</span><span class="sxs-lookup"><span data-stu-id="b32ce-137">CAPS LOCK</span></span>               | <span data-ttu-id="b32ce-138">20</span><span class="sxs-lookup"><span data-stu-id="b32ce-138">20</span></span>      |
| <span data-ttu-id="b32ce-139">Mayús (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="b32ce-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="b32ce-140">16</span><span class="sxs-lookup"><span data-stu-id="b32ce-140">16</span></span>      |
| <span data-ttu-id="b32ce-141">CTRL (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="b32ce-141">CTRL (left or right)</span></span>    | <span data-ttu-id="b32ce-142">17</span><span class="sxs-lookup"><span data-stu-id="b32ce-142">17</span></span>      |
| <span data-ttu-id="b32ce-143">ALT (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="b32ce-143">ALT (left or right)</span></span>     | <span data-ttu-id="b32ce-144">18</span><span class="sxs-lookup"><span data-stu-id="b32ce-144">18</span></span>      |
| <span data-ttu-id="b32ce-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="b32ce-145">SPACE</span></span>                   | <span data-ttu-id="b32ce-146">32</span><span class="sxs-lookup"><span data-stu-id="b32ce-146">32</span></span>      |
| <span data-ttu-id="b32ce-147">RETROCESO</span><span class="sxs-lookup"><span data-stu-id="b32ce-147">BACKSPACE</span></span>               | <span data-ttu-id="b32ce-148">8</span><span class="sxs-lookup"><span data-stu-id="b32ce-148">8</span></span>       |
| <span data-ttu-id="b32ce-149">ENTRAR</span><span class="sxs-lookup"><span data-stu-id="b32ce-149">ENTER</span></span>                   | <span data-ttu-id="b32ce-150">13</span><span class="sxs-lookup"><span data-stu-id="b32ce-150">13</span></span>      |
| <span data-ttu-id="b32ce-151">Tecla del logotipo de Windows, izquierda</span><span class="sxs-lookup"><span data-stu-id="b32ce-151">Windows logo key, left</span></span>  | <span data-ttu-id="b32ce-152">91</span><span class="sxs-lookup"><span data-stu-id="b32ce-152">91</span></span>      |
| <span data-ttu-id="b32ce-153">Tecla del logotipo de Windows, derecha</span><span class="sxs-lookup"><span data-stu-id="b32ce-153">Windows logo key, right</span></span> | <span data-ttu-id="b32ce-154">92</span><span class="sxs-lookup"><span data-stu-id="b32ce-154">92</span></span>      |
| <span data-ttu-id="b32ce-155">Clave de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b32ce-155">Application key</span></span>         | <span data-ttu-id="b32ce-156">93</span><span class="sxs-lookup"><span data-stu-id="b32ce-156">93</span></span>      |



 

<span data-ttu-id="b32ce-157">Valores de las teclas del panel numérico.</span><span class="sxs-lookup"><span data-stu-id="b32ce-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="b32ce-158">Clave</span><span class="sxs-lookup"><span data-stu-id="b32ce-158">Key</span></span>               | <span data-ttu-id="b32ce-159">Value</span><span class="sxs-lookup"><span data-stu-id="b32ce-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="b32ce-160">0-9</span><span class="sxs-lookup"><span data-stu-id="b32ce-160">0-9</span></span>               | <span data-ttu-id="b32ce-161">96-105</span><span class="sxs-lookup"><span data-stu-id="b32ce-161">96-105</span></span> |
| <span data-ttu-id="b32ce-162">BLOQ NUM</span><span class="sxs-lookup"><span data-stu-id="b32ce-162">NUM LOCK</span></span>          | <span data-ttu-id="b32ce-163">144</span><span class="sxs-lookup"><span data-stu-id="b32ce-163">144</span></span>    |
| <span data-ttu-id="b32ce-164">División (/)</span><span class="sxs-lookup"><span data-stu-id="b32ce-164">DIVIDE (/)</span></span>        | <span data-ttu-id="b32ce-165">111</span><span class="sxs-lookup"><span data-stu-id="b32ce-165">111</span></span>    |
| <span data-ttu-id="b32ce-166">MULTIPLICAr ( \* )</span><span class="sxs-lookup"><span data-stu-id="b32ce-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="b32ce-167">106</span><span class="sxs-lookup"><span data-stu-id="b32ce-167">106</span></span>    |
| <span data-ttu-id="b32ce-168">RESTA (-)</span><span class="sxs-lookup"><span data-stu-id="b32ce-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="b32ce-169">109</span><span class="sxs-lookup"><span data-stu-id="b32ce-169">109</span></span>    |
| <span data-ttu-id="b32ce-170">AGREGAR (+)</span><span class="sxs-lookup"><span data-stu-id="b32ce-170">ADD (+)</span></span>           | <span data-ttu-id="b32ce-171">107</span><span class="sxs-lookup"><span data-stu-id="b32ce-171">107</span></span>    |
| <span data-ttu-id="b32ce-172">Separador (entrar)</span><span class="sxs-lookup"><span data-stu-id="b32ce-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="b32ce-173">108</span><span class="sxs-lookup"><span data-stu-id="b32ce-173">108</span></span>    |
| <span data-ttu-id="b32ce-174">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="b32ce-174">DECIMAL (.)</span></span>       | <span data-ttu-id="b32ce-175">110</span><span class="sxs-lookup"><span data-stu-id="b32ce-175">110</span></span>    |



 

<span data-ttu-id="b32ce-176">Valores de las teclas de navegación.</span><span class="sxs-lookup"><span data-stu-id="b32ce-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="b32ce-177">Clave</span><span class="sxs-lookup"><span data-stu-id="b32ce-177">Key</span></span>         | <span data-ttu-id="b32ce-178">Value</span><span class="sxs-lookup"><span data-stu-id="b32ce-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="b32ce-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="b32ce-179">INSERT</span></span>      | <span data-ttu-id="b32ce-180">45</span><span class="sxs-lookup"><span data-stu-id="b32ce-180">45</span></span>    |
| <span data-ttu-id="b32ce-181">Delete</span><span class="sxs-lookup"><span data-stu-id="b32ce-181">DELETE</span></span>      | <span data-ttu-id="b32ce-182">46</span><span class="sxs-lookup"><span data-stu-id="b32ce-182">46</span></span>    |
| <span data-ttu-id="b32ce-183">INICIO</span><span class="sxs-lookup"><span data-stu-id="b32ce-183">HOME</span></span>        | <span data-ttu-id="b32ce-184">36</span><span class="sxs-lookup"><span data-stu-id="b32ce-184">36</span></span>    |
| <span data-ttu-id="b32ce-185">FIN</span><span class="sxs-lookup"><span data-stu-id="b32ce-185">END</span></span>         | <span data-ttu-id="b32ce-186">35</span><span class="sxs-lookup"><span data-stu-id="b32ce-186">35</span></span>    |
| <span data-ttu-id="b32ce-187">RE PÁG</span><span class="sxs-lookup"><span data-stu-id="b32ce-187">PAGE UP</span></span>     | <span data-ttu-id="b32ce-188">33</span><span class="sxs-lookup"><span data-stu-id="b32ce-188">33</span></span>    |
| <span data-ttu-id="b32ce-189">AV PÁG</span><span class="sxs-lookup"><span data-stu-id="b32ce-189">PAGE DOWN</span></span>   | <span data-ttu-id="b32ce-190">34</span><span class="sxs-lookup"><span data-stu-id="b32ce-190">34</span></span>    |
| <span data-ttu-id="b32ce-191">FLECHA ARRIBA</span><span class="sxs-lookup"><span data-stu-id="b32ce-191">UP ARROW</span></span>    | <span data-ttu-id="b32ce-192">38</span><span class="sxs-lookup"><span data-stu-id="b32ce-192">38</span></span>    |
| <span data-ttu-id="b32ce-193">FLECHA ABAJO</span><span class="sxs-lookup"><span data-stu-id="b32ce-193">DOWN ARROW</span></span>  | <span data-ttu-id="b32ce-194">40</span><span class="sxs-lookup"><span data-stu-id="b32ce-194">40</span></span>    |
| <span data-ttu-id="b32ce-195">FLECHA IZQUIERDA</span><span class="sxs-lookup"><span data-stu-id="b32ce-195">LEFT ARROW</span></span>  | <span data-ttu-id="b32ce-196">37</span><span class="sxs-lookup"><span data-stu-id="b32ce-196">37</span></span>    |
| <span data-ttu-id="b32ce-197">FLECHA DERECHA</span><span class="sxs-lookup"><span data-stu-id="b32ce-197">RIGHT ARROW</span></span> | <span data-ttu-id="b32ce-198">39</span><span class="sxs-lookup"><span data-stu-id="b32ce-198">39</span></span>    |



 

<span data-ttu-id="b32ce-199">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="b32ce-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="b32ce-200">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32ce-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="b32ce-201">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="b32ce-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32ce-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b32ce-202">Requirements</span></span>



| <span data-ttu-id="b32ce-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="b32ce-203">Requirement</span></span> | <span data-ttu-id="b32ce-204">Value</span><span class="sxs-lookup"><span data-stu-id="b32ce-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b32ce-205">Versión</span><span class="sxs-lookup"><span data-stu-id="b32ce-205">Version</span></span><br/> | <span data-ttu-id="b32ce-206">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="b32ce-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b32ce-207">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b32ce-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="b32ce-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b32ce-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32ce-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="b32ce-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32ce-210">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="b32ce-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





