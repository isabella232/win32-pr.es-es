---
title: Agregar el BUTTONELEMENT de juego
description: Agregar el BUTTONELEMENT de juego
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- crear máscaras, elemento BUTTONELEMENT
- Aspectos de Windows Media Player, elemento BUTTONELEMENT
- máscaras, elemento BUTTONELEMENT
- archivos de definición de máscara, elemento BUTTONELEMENT
- BUTTONELEMENT (elemento)
- elementos, BUTTONELEMENT
- crear máscaras, reproducir botones
- Aspectos de Windows Media Player, botones de reproducción
- máscaras, botones de reproducción
- archivos de definición de máscara, botones de reproducción
- Reproducir botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532170"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="f11e8-114">Agregar el BUTTONELEMENT de juego</span><span class="sxs-lookup"><span data-stu-id="f11e8-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="f11e8-115">Por último, puede Agregar los elementos **BUTTONELEMENT** que conectan los botones visuales de la pantalla a las acciones de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="f11e8-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="f11e8-116">Este es el núcleo de la piel y puede imaginarse como el cableado de la superficie de la piel a la maquinaria interna de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f11e8-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="f11e8-117">Los **BUTTONELEMENT** s se encuentran dentro de un **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="f11e8-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="f11e8-118">Siempre debe haber al menos un **BUTTONELEMENT** dentro de cada **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="f11e8-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="f11e8-119">Coloque el código **BUTTONELEMENT** de Play después del corchete angular de cierre de **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="f11e8-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="f11e8-120">Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón de reproducción:</span><span class="sxs-lookup"><span data-stu-id="f11e8-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="f11e8-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="f11e8-121">**mappingColor**</span></span>

<span data-ttu-id="f11e8-122">Este es el valor de color de una región en el archivo de imagen de asignación que creó antes.</span><span class="sxs-lookup"><span data-stu-id="f11e8-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="f11e8-123">En este caso, es el color verde sólido.</span><span class="sxs-lookup"><span data-stu-id="f11e8-123">In this case it is the solid green color.</span></span> <span data-ttu-id="f11e8-124">Este atributo es necesario para cualquier **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="f11e8-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="f11e8-125">Al definir este color, está indicando a Windows Media Player que asocie esta área de color con el código XML de este botón.</span><span class="sxs-lookup"><span data-stu-id="f11e8-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="f11e8-126">**Información sobre herramientas**</span><span class="sxs-lookup"><span data-stu-id="f11e8-126">**upToolTip**</span></span>

<span data-ttu-id="f11e8-127">Define el texto que se mostrará si el usuario mantiene el mouse sobre el botón.</span><span class="sxs-lookup"><span data-stu-id="f11e8-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="f11e8-128">No lo confunda con la imagen emergente que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="f11e8-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="f11e8-129">Una información sobre herramientas es un pequeño título de globo que tarda un momento en aparecer.</span><span class="sxs-lookup"><span data-stu-id="f11e8-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="f11e8-130">Sin embargo, la imagen de arte del mouse aparecerá al instante en el color y la forma que elija.</span><span class="sxs-lookup"><span data-stu-id="f11e8-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="f11e8-131">**AlHacerClic**</span><span class="sxs-lookup"><span data-stu-id="f11e8-131">**onClick**</span></span>

<span data-ttu-id="f11e8-132">Define el evento que se produce cuando se hace clic con el mouse en el botón.</span><span class="sxs-lookup"><span data-stu-id="f11e8-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="f11e8-133">El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función de JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**.</span><span class="sxs-lookup"><span data-stu-id="f11e8-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="f11e8-134">En este caso, el código JScript llama al método **URL** de Windows Media Player, que carga y comienza a reproducir un archivo llamado "Laure. WMA".</span><span class="sxs-lookup"><span data-stu-id="f11e8-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="f11e8-135">Tenga en cuenta que la línea finaliza con un punto y coma dentro de las comillas, que es una buena práctica de codificación de JScript.</span><span class="sxs-lookup"><span data-stu-id="f11e8-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="f11e8-136">Tenga en cuenta también el uso de comillas simples dentro de las comillas dobles para establecer el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f11e8-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="f11e8-137">Para obtener más información sobre JScript, vea [usar JScript](using-jscript.md) en la sección acerca de las máscaras de este SDK.</span><span class="sxs-lookup"><span data-stu-id="f11e8-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="f11e8-138">Observe que no hay ninguna etiqueta **BUTTONELEMENT** final.</span><span class="sxs-lookup"><span data-stu-id="f11e8-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="f11e8-139">Si un elemento no incluye otro elemento, puede cerrarlo con la barra diagonal justo antes del corchete angular de cierre.</span><span class="sxs-lookup"><span data-stu-id="f11e8-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="f11e8-140">Esto indica al XML que ha terminado con ese elemento.</span><span class="sxs-lookup"><span data-stu-id="f11e8-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="f11e8-141">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="f11e8-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="f11e8-142">y</span><span class="sxs-lookup"><span data-stu-id="f11e8-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="f11e8-143">transmita la misma información en XML.</span><span class="sxs-lookup"><span data-stu-id="f11e8-143">convey the same information in XML.</span></span>

<span data-ttu-id="f11e8-144">La eficacia de las máscaras proviene de usar controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="f11e8-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="f11e8-145">Si el usuario realiza alguna acción con un mouse, puede controlar ese evento con JScript.</span><span class="sxs-lookup"><span data-stu-id="f11e8-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="f11e8-146">El código puede ser una sola línea que hace que Windows Media Player haga algo sencillo como reproducir, o puede ser una aplicación completa escrita en JScript.</span><span class="sxs-lookup"><span data-stu-id="f11e8-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f11e8-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f11e8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11e8-148">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="f11e8-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




