---
title: Empezar con el tema y la vista
description: Empezar con el tema y la vista
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- crear máscaras, elemento de tema
- Aspectos de Windows Media Player, elemento THEME
- máscaras, elemento de tema
- archivos de definición de máscara, elemento THEME
- Elemento THEME
- crear máscaras, elemento VIEW
- Aspectos de Windows Media Player, elemento VIEW
- aspectos, elemento de vista
- archivos de definición de máscara, elemento de vista
- Elemento de vista
- elementos, vista
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903815"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="73458-115">Empezar con el tema y la vista</span><span class="sxs-lookup"><span data-stu-id="73458-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="73458-116">Cada máscara debe tener exactamente un elemento de **tema** y al menos un elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="73458-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="73458-117">Con el editor de texto, cree el siguiente texto:</span><span class="sxs-lookup"><span data-stu-id="73458-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="73458-118">Deje algunas líneas en blanco antes de la etiqueta de **vista** de cierre porque agregará más código aquí más adelante.</span><span class="sxs-lookup"><span data-stu-id="73458-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="73458-119">Guarde el archivo con cualquier nombre de archivo que desee, pero asegúrese de que la extensión es. WMS.</span><span class="sxs-lookup"><span data-stu-id="73458-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="73458-120">Por ejemplo, un nombre de archivo típico podría ser skinone. WMS.</span><span class="sxs-lookup"><span data-stu-id="73458-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="73458-121">Cada máscara debe empezar por <THEME> y terminar con </THEME>.</span><span class="sxs-lookup"><span data-stu-id="73458-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="73458-122">Solo puede tener un elemento de **tema** en la máscara, pero debe tener uno.</span><span class="sxs-lookup"><span data-stu-id="73458-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="73458-123">También debe tener al menos un elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="73458-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="73458-124">Puede tener más de una **vista**, pero este ejemplo solo tiene una.</span><span class="sxs-lookup"><span data-stu-id="73458-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="73458-125">Debe tener una apertura <VIEW> y un cierre <VIEW>. Tenga en cuenta que la etiqueta de apertura </VIEW> no cierra la etiqueta de inmediato, sino que incluye varios atributos antes del corchete angular de cierre (>).</span><span class="sxs-lookup"><span data-stu-id="73458-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="73458-126">En este ejemplo se usan los siguientes atributos en el elemento **Theme** :</span><span class="sxs-lookup"><span data-stu-id="73458-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="73458-127">**clippingColor**</span><span class="sxs-lookup"><span data-stu-id="73458-127">**clippingColor**</span></span>

<span data-ttu-id="73458-128">No siempre se necesita el atributo **clippingColor** si los bordes de la máscara son rectangulares.</span><span class="sxs-lookup"><span data-stu-id="73458-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="73458-129">La máscara de este ejemplo tiene forma ovalada, por lo que necesita un color de recorte para las partes de la máscara en las que desea ver el escritorio; esencialmente, todas las partes fuera de la elipse.</span><span class="sxs-lookup"><span data-stu-id="73458-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="73458-130">En esta máscara de ejemplo, usaremos un amarillo oscuro, que se especifica como " \# CCCC00" en formato web.</span><span class="sxs-lookup"><span data-stu-id="73458-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="73458-131">Los motivos de esta opción se proporcionan al [crear el archivo de imagen principal](creating-the-primary-art-file.md).</span><span class="sxs-lookup"><span data-stu-id="73458-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="73458-132">Esencialmente, este valor siempre será un número que se obtiene del programa de arte.</span><span class="sxs-lookup"><span data-stu-id="73458-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="73458-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="73458-133">**backgroundImage**</span></span>

<span data-ttu-id="73458-134">Este es el nombre del archivo de imagen principal.</span><span class="sxs-lookup"><span data-stu-id="73458-134">This is the name of the primary art file.</span></span> <span data-ttu-id="73458-135">Debe ser el nombre de archivo y la ruta de acceso exactos del archivo de imagen principal.</span><span class="sxs-lookup"><span data-stu-id="73458-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="73458-136">Solo se admiten archivos BMP, JPG, GIF y PNG, y se recomienda usar BMP.</span><span class="sxs-lookup"><span data-stu-id="73458-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="73458-137">**titleBar**</span><span class="sxs-lookup"><span data-stu-id="73458-137">**titleBar**</span></span>

<span data-ttu-id="73458-138">Esta máscara no tiene una **TitleBar**, por lo que el valor será "false".</span><span class="sxs-lookup"><span data-stu-id="73458-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="73458-139">Solo deseará una barra de título si desea que la máscara tenga un color de fondo y sea rectangular.</span><span class="sxs-lookup"><span data-stu-id="73458-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="73458-140">Asegúrese de colocar el corchete angular de cierre (>) después del valor de la **TitleBar** para indicar que ha terminado de definir la **vista**.</span><span class="sxs-lookup"><span data-stu-id="73458-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="73458-141">Deje unas cuantas líneas en blanco antes de la **vista** de cierre y las etiquetas de **tema** .</span><span class="sxs-lookup"><span data-stu-id="73458-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="73458-142">Necesitará las líneas para el código que agregará más adelante.</span><span class="sxs-lookup"><span data-stu-id="73458-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73458-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73458-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73458-144">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="73458-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




