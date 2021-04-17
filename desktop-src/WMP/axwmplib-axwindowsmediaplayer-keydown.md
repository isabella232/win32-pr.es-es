---
title: Evento KeyDown del objeto AxWindowsMediaPlayer
description: El evento KeyDown tiene lugar cuando se presiona una tecla. | Evento KeyDown del objeto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700167"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6862a-105">Evento KeyDown del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="6862a-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6862a-106">El evento KeyDown tiene lugar cuando se presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="6862a-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="6862a-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="6862a-107">Event Data</span></span>

<span data-ttu-id="6862a-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="6862a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="6862a-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="6862a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="6862a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6862a-110">Property</span></span>    | <span data-ttu-id="6862a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6862a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6862a-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="6862a-112">nKeyCode</span></span>    | <span data-ttu-id="6862a-113">System. Int16Specifies Qué tecla física está presionada.</span><span class="sxs-lookup"><span data-stu-id="6862a-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="6862a-114">Para ver los valores posibles, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6862a-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6862a-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="6862a-115">nShiftState</span></span> | <span data-ttu-id="6862a-116">El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="6862a-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="6862a-117">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6862a-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="6862a-118">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="6862a-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="6862a-119">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="6862a-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6862a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6862a-120">Remarks</span></span>

<span data-ttu-id="6862a-121">La propiedad **nKeyCode** especifica una clave física.</span><span class="sxs-lookup"><span data-stu-id="6862a-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="6862a-122">En las tablas siguientes se muestran los posibles valores de las claves principales de un teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="6862a-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="6862a-123">Valores de las claves principales.</span><span class="sxs-lookup"><span data-stu-id="6862a-123">Values for the main keys.</span></span>



| <span data-ttu-id="6862a-124">Clave</span><span class="sxs-lookup"><span data-stu-id="6862a-124">Key</span></span>                     | <span data-ttu-id="6862a-125">Value</span><span class="sxs-lookup"><span data-stu-id="6862a-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="6862a-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="6862a-126">A-Z</span></span>                     | <span data-ttu-id="6862a-127">65-90</span><span class="sxs-lookup"><span data-stu-id="6862a-127">65-90</span></span>   |
| <span data-ttu-id="6862a-128">0-9</span><span class="sxs-lookup"><span data-stu-id="6862a-128">0-9</span></span>                     | <span data-ttu-id="6862a-129">48-56</span><span class="sxs-lookup"><span data-stu-id="6862a-129">48-56</span></span>   |
| <span data-ttu-id="6862a-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="6862a-130">F1-F12</span></span>                  | <span data-ttu-id="6862a-131">112-123</span><span class="sxs-lookup"><span data-stu-id="6862a-131">112-123</span></span> |
| <span data-ttu-id="6862a-132">ESC</span><span class="sxs-lookup"><span data-stu-id="6862a-132">ESC</span></span>                     | <span data-ttu-id="6862a-133">27</span><span class="sxs-lookup"><span data-stu-id="6862a-133">27</span></span>      |
| <span data-ttu-id="6862a-134">TAB</span><span class="sxs-lookup"><span data-stu-id="6862a-134">TAB</span></span>                     | <span data-ttu-id="6862a-135">9</span><span class="sxs-lookup"><span data-stu-id="6862a-135">9</span></span>       |
| <span data-ttu-id="6862a-136">Bloq Mayús</span><span class="sxs-lookup"><span data-stu-id="6862a-136">CAPS LOCK</span></span>               | <span data-ttu-id="6862a-137">20</span><span class="sxs-lookup"><span data-stu-id="6862a-137">20</span></span>      |
| <span data-ttu-id="6862a-138">Mayús (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="6862a-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="6862a-139">16</span><span class="sxs-lookup"><span data-stu-id="6862a-139">16</span></span>      |
| <span data-ttu-id="6862a-140">CTRL (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="6862a-140">CTRL (left or right)</span></span>    | <span data-ttu-id="6862a-141">17</span><span class="sxs-lookup"><span data-stu-id="6862a-141">17</span></span>      |
| <span data-ttu-id="6862a-142">ALT (izquierda o derecha)</span><span class="sxs-lookup"><span data-stu-id="6862a-142">ALT (left or right)</span></span>     | <span data-ttu-id="6862a-143">18</span><span class="sxs-lookup"><span data-stu-id="6862a-143">18</span></span>      |
| <span data-ttu-id="6862a-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="6862a-144">SPACE</span></span>                   | <span data-ttu-id="6862a-145">32</span><span class="sxs-lookup"><span data-stu-id="6862a-145">32</span></span>      |
| <span data-ttu-id="6862a-146">RETROCESO</span><span class="sxs-lookup"><span data-stu-id="6862a-146">BACKSPACE</span></span>               | <span data-ttu-id="6862a-147">8</span><span class="sxs-lookup"><span data-stu-id="6862a-147">8</span></span>       |
| <span data-ttu-id="6862a-148">ENTRAR</span><span class="sxs-lookup"><span data-stu-id="6862a-148">ENTER</span></span>                   | <span data-ttu-id="6862a-149">13</span><span class="sxs-lookup"><span data-stu-id="6862a-149">13</span></span>      |
| <span data-ttu-id="6862a-150">Tecla del logotipo de Windows, izquierda</span><span class="sxs-lookup"><span data-stu-id="6862a-150">Windows logo key, left</span></span>  | <span data-ttu-id="6862a-151">91</span><span class="sxs-lookup"><span data-stu-id="6862a-151">91</span></span>      |
| <span data-ttu-id="6862a-152">Tecla del logotipo de Windows, derecha</span><span class="sxs-lookup"><span data-stu-id="6862a-152">Windows logo key, right</span></span> | <span data-ttu-id="6862a-153">92</span><span class="sxs-lookup"><span data-stu-id="6862a-153">92</span></span>      |
| <span data-ttu-id="6862a-154">Clave de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6862a-154">Application key</span></span>         | <span data-ttu-id="6862a-155">93</span><span class="sxs-lookup"><span data-stu-id="6862a-155">93</span></span>      |



 

<span data-ttu-id="6862a-156">Valores de las teclas del panel numérico.</span><span class="sxs-lookup"><span data-stu-id="6862a-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="6862a-157">Clave</span><span class="sxs-lookup"><span data-stu-id="6862a-157">Key</span></span>               | <span data-ttu-id="6862a-158">Value</span><span class="sxs-lookup"><span data-stu-id="6862a-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="6862a-159">0-9</span><span class="sxs-lookup"><span data-stu-id="6862a-159">0-9</span></span>               | <span data-ttu-id="6862a-160">96-105</span><span class="sxs-lookup"><span data-stu-id="6862a-160">96-105</span></span> |
| <span data-ttu-id="6862a-161">BLOQ NUM</span><span class="sxs-lookup"><span data-stu-id="6862a-161">NUM LOCK</span></span>          | <span data-ttu-id="6862a-162">144</span><span class="sxs-lookup"><span data-stu-id="6862a-162">144</span></span>    |
| <span data-ttu-id="6862a-163">División (/)</span><span class="sxs-lookup"><span data-stu-id="6862a-163">DIVIDE (/)</span></span>        | <span data-ttu-id="6862a-164">111</span><span class="sxs-lookup"><span data-stu-id="6862a-164">111</span></span>    |
| <span data-ttu-id="6862a-165">MULTIPLICAr ( \* )</span><span class="sxs-lookup"><span data-stu-id="6862a-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="6862a-166">106</span><span class="sxs-lookup"><span data-stu-id="6862a-166">106</span></span>    |
| <span data-ttu-id="6862a-167">RESTA (-)</span><span class="sxs-lookup"><span data-stu-id="6862a-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="6862a-168">109</span><span class="sxs-lookup"><span data-stu-id="6862a-168">109</span></span>    |
| <span data-ttu-id="6862a-169">AGREGAR (+)</span><span class="sxs-lookup"><span data-stu-id="6862a-169">ADD (+)</span></span>           | <span data-ttu-id="6862a-170">107</span><span class="sxs-lookup"><span data-stu-id="6862a-170">107</span></span>    |
| <span data-ttu-id="6862a-171">Separador (entrar)</span><span class="sxs-lookup"><span data-stu-id="6862a-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="6862a-172">108</span><span class="sxs-lookup"><span data-stu-id="6862a-172">108</span></span>    |
| <span data-ttu-id="6862a-173">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="6862a-173">DECIMAL (.)</span></span>       | <span data-ttu-id="6862a-174">110</span><span class="sxs-lookup"><span data-stu-id="6862a-174">110</span></span>    |



 

<span data-ttu-id="6862a-175">Valores de las teclas de navegación.</span><span class="sxs-lookup"><span data-stu-id="6862a-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="6862a-176">Clave</span><span class="sxs-lookup"><span data-stu-id="6862a-176">Key</span></span>         | <span data-ttu-id="6862a-177">Value</span><span class="sxs-lookup"><span data-stu-id="6862a-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="6862a-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="6862a-178">INSERT</span></span>      | <span data-ttu-id="6862a-179">45</span><span class="sxs-lookup"><span data-stu-id="6862a-179">45</span></span>    |
| <span data-ttu-id="6862a-180">Delete</span><span class="sxs-lookup"><span data-stu-id="6862a-180">DELETE</span></span>      | <span data-ttu-id="6862a-181">46</span><span class="sxs-lookup"><span data-stu-id="6862a-181">46</span></span>    |
| <span data-ttu-id="6862a-182">INICIO</span><span class="sxs-lookup"><span data-stu-id="6862a-182">HOME</span></span>        | <span data-ttu-id="6862a-183">36</span><span class="sxs-lookup"><span data-stu-id="6862a-183">36</span></span>    |
| <span data-ttu-id="6862a-184">FIN</span><span class="sxs-lookup"><span data-stu-id="6862a-184">END</span></span>         | <span data-ttu-id="6862a-185">35</span><span class="sxs-lookup"><span data-stu-id="6862a-185">35</span></span>    |
| <span data-ttu-id="6862a-186">RE PÁG</span><span class="sxs-lookup"><span data-stu-id="6862a-186">PAGE UP</span></span>     | <span data-ttu-id="6862a-187">33</span><span class="sxs-lookup"><span data-stu-id="6862a-187">33</span></span>    |
| <span data-ttu-id="6862a-188">AV PÁG</span><span class="sxs-lookup"><span data-stu-id="6862a-188">PAGE DOWN</span></span>   | <span data-ttu-id="6862a-189">34</span><span class="sxs-lookup"><span data-stu-id="6862a-189">34</span></span>    |
| <span data-ttu-id="6862a-190">FLECHA ARRIBA</span><span class="sxs-lookup"><span data-stu-id="6862a-190">UP ARROW</span></span>    | <span data-ttu-id="6862a-191">38</span><span class="sxs-lookup"><span data-stu-id="6862a-191">38</span></span>    |
| <span data-ttu-id="6862a-192">FLECHA ABAJO</span><span class="sxs-lookup"><span data-stu-id="6862a-192">DOWN ARROW</span></span>  | <span data-ttu-id="6862a-193">40</span><span class="sxs-lookup"><span data-stu-id="6862a-193">40</span></span>    |
| <span data-ttu-id="6862a-194">FLECHA IZQUIERDA</span><span class="sxs-lookup"><span data-stu-id="6862a-194">LEFT ARROW</span></span>  | <span data-ttu-id="6862a-195">37</span><span class="sxs-lookup"><span data-stu-id="6862a-195">37</span></span>    |
| <span data-ttu-id="6862a-196">FLECHA DERECHA</span><span class="sxs-lookup"><span data-stu-id="6862a-196">RIGHT ARROW</span></span> | <span data-ttu-id="6862a-197">39</span><span class="sxs-lookup"><span data-stu-id="6862a-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="6862a-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6862a-198">Requirements</span></span>



| <span data-ttu-id="6862a-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="6862a-199">Requirement</span></span> | <span data-ttu-id="6862a-200">Value</span><span class="sxs-lookup"><span data-stu-id="6862a-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6862a-201">Versión</span><span class="sxs-lookup"><span data-stu-id="6862a-201">Version</span></span><br/>   | <span data-ttu-id="6862a-202">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="6862a-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6862a-203">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6862a-203">Namespace</span></span><br/> | <span data-ttu-id="6862a-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6862a-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6862a-205">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="6862a-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6862a-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6862a-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6862a-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="6862a-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6862a-208">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6862a-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





