---
title: Ejemplo de arte sencillo
description: Ejemplo de arte sencillo
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, ejemplos
- Aspectos de Windows Media Player, ejemplos
- máscaras, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775546"
---
# <a name="simple-art-example"></a><span data-ttu-id="cd099-109">Ejemplo de arte sencillo</span><span class="sxs-lookup"><span data-stu-id="cd099-109">Simple Art Example</span></span>

<span data-ttu-id="cd099-110">Se necesitan tres archivos de imagen para crear una máscara simple con dos botones.</span><span class="sxs-lookup"><span data-stu-id="cd099-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="cd099-111">Se requiere una imagen principal y una imagen de asignación, y una imagen alternativa proporciona una indicación visual al usuario de que se hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="cd099-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="cd099-112">Estos archivos de imágenes se crearon en un programa de arte que usa capas.</span><span class="sxs-lookup"><span data-stu-id="cd099-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="cd099-113">El uso de capas facilita la tarea de asegurarse de que la imagen principal, la asignación y las imágenes alternativas tienen el mismo tamaño y se alinean entre sí.</span><span class="sxs-lookup"><span data-stu-id="cd099-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="cd099-114">Las instrucciones detalladas sobre la creación de material gráfico se encuentran en la [Guía de creación de máscaras](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="cd099-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="cd099-115">Imagen principal</span><span class="sxs-lookup"><span data-stu-id="cd099-115">Primary Image</span></span>

<span data-ttu-id="cd099-116">La imagen principal es un óvalo amarillo simple con dos botones, uno rosa para iniciar Windows Media Player y el botón púrpura para detenerlo.</span><span class="sxs-lookup"><span data-stu-id="cd099-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="cd099-117">El fondo es un amarillo ligeramente más oscuro que el óvalo.</span><span class="sxs-lookup"><span data-stu-id="cd099-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="cd099-118">Esta imagen se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-118">This image is shown in the following illustration.</span></span>

![imagen principal](images/absam01b.png)

<span data-ttu-id="cd099-120">La imagen principal era de las siguientes imágenes, cada una en una capa independiente.</span><span class="sxs-lookup"><span data-stu-id="cd099-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="cd099-121">En primer lugar, se creó un óvalo con un efecto de bisel y de relieve de capa.</span><span class="sxs-lookup"><span data-stu-id="cd099-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="cd099-122">Esta imagen se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-122">This image is shown in the following illustration.</span></span>

![imagen ovalada](images/absam01s.png)

<span data-ttu-id="cd099-124">A continuación, se crearon los dos botones, también con efectos de bisel y relieve de capa.</span><span class="sxs-lookup"><span data-stu-id="cd099-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="cd099-125">Esto se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-125">This is shown in the following illustration.</span></span>

![dos botones](images/absam01p.png)

<span data-ttu-id="cd099-127">A continuación, se creó el fondo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cd099-127">Next the image background was created.</span></span> <span data-ttu-id="cd099-128">Se ha elegido un amarillo ligeramente más oscuro para que no se detecte ningún suavizado de contorno entre el óvalo y el fondo.</span><span class="sxs-lookup"><span data-stu-id="cd099-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="cd099-129">El valor de color es \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="cd099-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="cd099-130">Esta imagen se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-130">This image is shown in the following illustration.</span></span>

![imagen de fondo](images/absam01y.png)

<span data-ttu-id="cd099-132">Las capas que contenían estas imágenes se hicieron visibles y se guardan como una copia en formato de mapa de bits, con lo que se crea la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="cd099-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="cd099-133">El atributo **BackgroundImage** del elemento **View** usará la imagen compuesta principal.</span><span class="sxs-lookup"><span data-stu-id="cd099-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="cd099-134">Imagen de asignación</span><span class="sxs-lookup"><span data-stu-id="cd099-134">Mapping Image</span></span>

<span data-ttu-id="cd099-135">Se necesita una imagen de asignación para especificar Cuándo y dónde se hace clic en una máscara.</span><span class="sxs-lookup"><span data-stu-id="cd099-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="cd099-136">Se creó una imagen de asignación con un área roja y un área verde.</span><span class="sxs-lookup"><span data-stu-id="cd099-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="cd099-137">Esta imagen se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-137">This image is shown in the following illustration.</span></span>

![imagen de asignación](images/absam01m.png)

<span data-ttu-id="cd099-139">El área verde se usará para identificar el área de la máscara que iniciará Windows Media Player y se utilizará el área roja para detenerla.</span><span class="sxs-lookup"><span data-stu-id="cd099-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="cd099-140">La imagen de asignación tiene el mismo tamaño que la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="cd099-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="cd099-141">La imagen de asignación se creó copiando la capa de botón en una nueva capa y desactivando el efecto de bisel y relieve.</span><span class="sxs-lookup"><span data-stu-id="cd099-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="cd099-142">Se necesitan imágenes planas para la asignación, ya que Windows Media Player buscará valores de color único en cada área.</span><span class="sxs-lookup"><span data-stu-id="cd099-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="cd099-143">Solo puede buscar un color que defina, como rojo ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="cd099-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="cd099-144">Si la imagen tiene un bisel u otro efecto, no todas serán las rojas exactas que necesite.</span><span class="sxs-lookup"><span data-stu-id="cd099-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="cd099-145">Para que los botones de asignación sean un color sencillo de recordar, las imágenes se rellenaron con rojo puro y verde puro, pero se puede usar cualquier color.</span><span class="sxs-lookup"><span data-stu-id="cd099-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="cd099-146">Tendrá que recordar los números de color del mapa para que se puedan escribir en el archivo de definición de máscara XML.</span><span class="sxs-lookup"><span data-stu-id="cd099-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="cd099-147">En este caso, el color rojo es \# FF0000 y el verde es \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="cd099-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="cd099-148">A continuación, con solo la nueva capa visible, la imagen se guardó como copia en un archivo BMP.</span><span class="sxs-lookup"><span data-stu-id="cd099-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="cd099-149">Será llamado por el atributo **mappingImage** del elemento **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="cd099-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="cd099-150">Imagen alternativa</span><span class="sxs-lookup"><span data-stu-id="cd099-150">Alternate Image</span></span>

<span data-ttu-id="cd099-151">No se requieren imágenes alternativas, pero son muy útiles para proporcionar indicaciones visuales al usuario.</span><span class="sxs-lookup"><span data-stu-id="cd099-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="cd099-152">En este caso, se recomienda una imagen de mantener el mouse para que el usuario sepa en qué áreas se puede hacer clic.</span><span class="sxs-lookup"><span data-stu-id="cd099-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="cd099-153">Se creó una imagen alternativa con dos botones amarillos.</span><span class="sxs-lookup"><span data-stu-id="cd099-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="cd099-154">Esto se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="cd099-154">This is shown in the following illustration.</span></span>

![imagen de desplazamiento](images/absam01h.png)

<span data-ttu-id="cd099-156">La imagen alternativa se creó copiando la capa de botón original en una nueva capa y, a continuación, cambiando el color de relleno a amarillo.</span><span class="sxs-lookup"><span data-stu-id="cd099-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="cd099-157">Se mantuvo el efecto de bisel y de relieve.</span><span class="sxs-lookup"><span data-stu-id="cd099-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="cd099-158">A continuación, se creó una nueva capa y se agregaron imágenes: la flecha indica "reproducir" y el cuadrado indica "detener".</span><span class="sxs-lookup"><span data-stu-id="cd099-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="cd099-159">A continuación, con solo el nuevo botón amarillo y las capas de tipo visibles, la imagen se guardó como una copia en un archivo de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="cd099-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="cd099-160">El resultado es que cuando el mouse se desplaza sobre un área definida por la imagen de asignación, se muestra la imagen de mantener el puntero, alertar al lector de que si hace clic en ese punto, pueden reproducir o detener Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cd099-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="cd099-161">Imagen final</span><span class="sxs-lookup"><span data-stu-id="cd099-161">Final Image</span></span>

<span data-ttu-id="cd099-162">Esta es la imagen final de la máscara.</span><span class="sxs-lookup"><span data-stu-id="cd099-162">Here is the final image of the skin.</span></span>

![imagen final](images/absam01f.png)

<span data-ttu-id="cd099-164">Y esta es la imagen que verá si mantiene el puntero sobre el botón rosa de la derecha.</span><span class="sxs-lookup"><span data-stu-id="cd099-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![mantener el mouse sobre el botón derecho](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="cd099-166">Código XML para el ejemplo de arte</span><span class="sxs-lookup"><span data-stu-id="cd099-166">XML Code for the Art Example</span></span>

<span data-ttu-id="cd099-167">Los detalles de cómo escribir código XML se proporcionan en la [Guía de creación de máscaras](skin-creation-guide.md), pero para mostrar la cantidad de código que se necesita para crear una máscara de trabajo, este es el código de la ilustración en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cd099-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="cd099-168">Los botones predefinidos se utilizan para las funciones Play y STOP.</span><span class="sxs-lookup"><span data-stu-id="cd099-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="cd099-169">Debe cargar un archivo o una lista de reproducción desde el delimitador de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cd099-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="cd099-170">Cuando Windows Media Player cambia al modo de máscara, aparece un cuadro pequeño en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cd099-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="cd099-171">Este cuadro se denomina "delimitador".</span><span class="sxs-lookup"><span data-stu-id="cd099-171">This box is called the "anchor".</span></span> <span data-ttu-id="cd099-172">Al hacer clic en el delimitador, se proporciona la funcionalidad mínima necesaria, en caso de que una máscara no proporcione una manera de volver al modo completo de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cd099-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="cd099-173">El usuario puede cambiar entre modos mediante el menú **Ver** si está en modo completo o haciendo clic en el delimitador si está en modo de máscara.</span><span class="sxs-lookup"><span data-stu-id="cd099-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="cd099-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd099-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd099-175">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="cd099-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




