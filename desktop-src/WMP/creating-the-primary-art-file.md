---
title: Crear el archivo de imagen principal
description: Crear el archivo de imagen principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- crear máscaras, archivos de imagen principal
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, imágenes principales
- Aspectos de Windows Media Player, imágenes principales
- máscaras, imágenes principales
- imágenes principales en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104554130"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="8c776-111">Crear el archivo de imagen principal</span><span class="sxs-lookup"><span data-stu-id="8c776-111">Creating the Primary Art File</span></span>

<span data-ttu-id="8c776-112">El archivo de imagen principal contendrá el arte que el usuario de la máscara ve en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="8c776-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="8c776-113">En este caso, creará imágenes en diferentes capas del programa de arte.</span><span class="sxs-lookup"><span data-stu-id="8c776-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="8c776-114">El motivo del uso de capas es que se copiarán niveles específicos posteriormente para crear archivos de mapa y archivos de imagen alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c776-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="8c776-115">Para crear el archivo de imagen principal, creará las siguientes capas en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="8c776-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="8c776-116">Capa de fondo de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-116">Skin background layer</span></span>

<span data-ttu-id="8c776-117">Este es el color que será transparente cuando se muestre la máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="8c776-118">Cree una capa por primera vez, pero elija el color final de esta capa después de elegir un color para la capa de contenedor de máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="8c776-119">Este color debe ser similar a, pero no igual que el de la capa de contenedor de máscara, para ocultar los efectos de suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="8c776-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="8c776-120">Capa de contenedor de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-120">Skin container layer</span></span>

<span data-ttu-id="8c776-121">Esta es la imagen que formará el contorno de la máscara y será lo que vea el usuario.</span><span class="sxs-lookup"><span data-stu-id="8c776-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="8c776-122">También será el contenedor de los dos botones de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8c776-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="8c776-123">Considere la piel como un contenedor para los controles de interfaz de usuario, como botones, controles deslizantes, etc.</span><span class="sxs-lookup"><span data-stu-id="8c776-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="8c776-124">En este ejemplo, el contenedor es un óvalo amarillo.</span><span class="sxs-lookup"><span data-stu-id="8c776-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="8c776-125">Capas de los botones Reproducir y cerrar</span><span class="sxs-lookup"><span data-stu-id="8c776-125">Play and Close button layers</span></span>

<span data-ttu-id="8c776-126">Estos son los dos controles de interfaz de usuario que utiliza este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8c776-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="8c776-127">Los colocará en capas independientes para que pueda ajustarlos fácilmente o copiarlos más adelante.</span><span class="sxs-lookup"><span data-stu-id="8c776-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="8c776-128">Antes de crear las capas, debe crear el archivo que contendrá las capas.</span><span class="sxs-lookup"><span data-stu-id="8c776-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="8c776-129">Inicie Photoshop y cree un nuevo archivo de 100 píxeles de alto y 200 píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="8c776-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="8c776-130">El archivo que se usa para crear la imagen de este ejemplo se denomina tiny.psd y se incluye con el SDK.</span><span class="sxs-lookup"><span data-stu-id="8c776-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="8c776-131">Todas las instrucciones se proporcionan en términos de Photoshop, pero cualquier otro programa de arte se puede usar para crear máscaras siempre que se pueda guardar en uno de los formatos de archivo admitidos por la Media Player de Windows (BMP, GIF, JPG y PNG).</span><span class="sxs-lookup"><span data-stu-id="8c776-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="8c776-132">Encontrará más fácil la creación de máscaras si usa un programa artístico con capas, como Adobe Photoshop, Jasc Paint Shop Pro o Jedor viscosidad.</span><span class="sxs-lookup"><span data-stu-id="8c776-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="8c776-133">Las capas son muy útiles porque las imágenes se deben alinear correctamente para la asignación de imágenes y la presentación de imágenes alternativas.</span><span class="sxs-lookup"><span data-stu-id="8c776-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="8c776-134">Capa de fondo de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-134">Skin Background Layer</span></span>

<span data-ttu-id="8c776-135">Cree una nueva capa y asígnele el nombre "fondo de máscara".</span><span class="sxs-lookup"><span data-stu-id="8c776-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="8c776-136">Se convertirá en el color de transparencia que definirá en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="8c776-137">Espere hasta que se elija el color del contenedor de máscara antes de rellenar el nivel de fondo de la máscara con un color específico.</span><span class="sxs-lookup"><span data-stu-id="8c776-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="8c776-138">Capa de contenedor de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-138">Skin Container Layer</span></span>

<span data-ttu-id="8c776-139">A continuación, cree una nueva capa y llámela "contenedor de máscara".</span><span class="sxs-lookup"><span data-stu-id="8c776-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="8c776-140">Esto definirá los bordes de la máscara y será el contenedor de los botones.</span><span class="sxs-lookup"><span data-stu-id="8c776-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="8c776-141">Elija un color de primer plano para la forma mediante los controles deslizantes de color Web.</span><span class="sxs-lookup"><span data-stu-id="8c776-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="8c776-142">En este ejemplo, \# se ha elegido el color "DBDD11".</span><span class="sxs-lookup"><span data-stu-id="8c776-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="8c776-143">A continuación, cree una forma ovalada.</span><span class="sxs-lookup"><span data-stu-id="8c776-143">Next create an oval shape.</span></span> <span data-ttu-id="8c776-144">La manera más fácil es usar la herramienta eliptical marquesina y crear una selección ovalada.</span><span class="sxs-lookup"><span data-stu-id="8c776-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="8c776-145">Cuando haya creado una selección de óvalo que tenga el tamaño y la forma que desee, rellene la selección con el color de primer plano y cancele la selección.</span><span class="sxs-lookup"><span data-stu-id="8c776-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="8c776-146">Por último, para que este aspecto sea un poco más interesante, aplique el efecto de capa de bisel y relieve con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="8c776-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="8c776-147">La capa de contenedor de máscara debe ser similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8c776-147">Your skin container layer should look like the following illustration.</span></span>

![capa de contenedor de máscara](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="8c776-149">Color de máscara de fondo</span><span class="sxs-lookup"><span data-stu-id="8c776-149">Background Skin Color</span></span>

<span data-ttu-id="8c776-150">Ahora que ha elegido un color de primer plano para la forma de contenedor de máscara, puede elegir un color similar para la capa de fondo de la máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="8c776-151">No desea el mismo color exacto o el contenedor de máscara también será transparente.</span><span class="sxs-lookup"><span data-stu-id="8c776-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="8c776-152">De hecho, asegúrese de que no usa este color exacto en cualquier parte de la máscara, ni siquiera en fotografías, ya que, siempre que aparezca este color, aparecerá la imagen de escritorio en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8c776-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="8c776-153">Desea un color cerca del color del contenedor de máscara para evitar efectos de suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="8c776-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="8c776-154">Por ejemplo, si tiene un fondo negro, algunos bits de negro pueden aparecer en torno al borde de la piel.</span><span class="sxs-lookup"><span data-stu-id="8c776-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="8c776-155">Al elegir un color cerca del color del contenedor de máscara, los píxeles aislados que se muestran en el proceso de suavizado de contorno no se apreciarán.</span><span class="sxs-lookup"><span data-stu-id="8c776-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="8c776-156">El suavizado de contorno es el proceso de suavizar los bordes de las formas inclinadas o curvas.</span><span class="sxs-lookup"><span data-stu-id="8c776-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="8c776-157">Suavizado de contorno crea nuevos colores, para píxeles a lo largo de los bordes de una forma, que son una combinación del color de primer plano y el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="8c776-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="8c776-158">Algunos de estos colores, entre otros, pueden provocar que se pierdan los píxeles cuando el color de fondo se hace transparente.</span><span class="sxs-lookup"><span data-stu-id="8c776-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="8c776-159">La capa de fondo de la máscara debe ser similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8c776-159">Your skin background layer should look like the following illustration.</span></span>

![capa de máscara de fondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="8c776-161">Capas de los botones Reproducir y cerrar</span><span class="sxs-lookup"><span data-stu-id="8c776-161">Play and Close Button Layers</span></span>

<span data-ttu-id="8c776-162">Cree una nueva capa y asígnele el nombre "botón Cerrar".</span><span class="sxs-lookup"><span data-stu-id="8c776-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="8c776-163">Con la herramienta de selección de marquesina eliptical, cree un círculo y colóquelo en el lado izquierdo de la imagen global.</span><span class="sxs-lookup"><span data-stu-id="8c776-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="8c776-164">Active la visibilidad del archivo contenedor de máscara para ayudar a colocar la selección.</span><span class="sxs-lookup"><span data-stu-id="8c776-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="8c776-165">Cuando esté satisfecho con la selección de ubicación, rellene la selección con cualquier color (excepto el color del contenedor de máscara o el fondo de la máscara).</span><span class="sxs-lookup"><span data-stu-id="8c776-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="8c776-166">En este ejemplo, se ha elegido un color púrpura.</span><span class="sxs-lookup"><span data-stu-id="8c776-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="8c776-167">No es necesario recordar el número del color.</span><span class="sxs-lookup"><span data-stu-id="8c776-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="8c776-168">A continuación, cancele la selección y aplique otro efecto de la capa de bisel y de relieve predeterminados.</span><span class="sxs-lookup"><span data-stu-id="8c776-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="8c776-169">Si desea aplicar efectos que no son de capa al botón, haga una copia del original para su uso posterior en la asignación.</span><span class="sxs-lookup"><span data-stu-id="8c776-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="8c776-170">El botón Cerrar debe ser similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8c776-170">Your Close button should look like the following illustration.</span></span>

![botón Cerrar](images/g01qbut.png)

<span data-ttu-id="8c776-172">Cree una nueva capa y asígnele el nombre "botón reproducir".</span><span class="sxs-lookup"><span data-stu-id="8c776-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="8c776-173">Utilice las mismas técnicas que hizo para el botón Cerrar, pero asígnele un color diferente.</span><span class="sxs-lookup"><span data-stu-id="8c776-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="8c776-174">En este caso, se ha elegido un color de botón rosa, pero se puede usar cualquier color siempre que no sea el mismo color que el contenedor de máscara (porque se fusionaría en el contenedor) o el color de fondo de la máscara (porque se convertiría en transparente).</span><span class="sxs-lookup"><span data-stu-id="8c776-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="8c776-175">El botón de reproducción debería tener un aspecto similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8c776-175">Your Play button should look like the following illustration.</span></span>

![botón reproducir](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="8c776-177">Combinar capas y guardar</span><span class="sxs-lookup"><span data-stu-id="8c776-177">Combine Layers and Save</span></span>

<span data-ttu-id="8c776-178">Ahora está listo para crear el archivo de imagen principal.</span><span class="sxs-lookup"><span data-stu-id="8c776-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="8c776-179">Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):</span><span class="sxs-lookup"><span data-stu-id="8c776-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="8c776-180">Botón de reproducción</span><span class="sxs-lookup"><span data-stu-id="8c776-180">Play button</span></span>

<span data-ttu-id="8c776-181">Botón Cerrar</span><span class="sxs-lookup"><span data-stu-id="8c776-181">Close button</span></span>

<span data-ttu-id="8c776-182">Contenedor de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-182">Skin container</span></span>

<span data-ttu-id="8c776-183">Fondo de máscara</span><span class="sxs-lookup"><span data-stu-id="8c776-183">Skin background</span></span>

<span data-ttu-id="8c776-184">Guarde en un archivo nuevo con el comando Guardar una copia del menú archivo.</span><span class="sxs-lookup"><span data-stu-id="8c776-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="8c776-185">Seleccione la opción BMP en la parte guardar como del cuadro de diálogo guardar una copia y escriba un nombre de archivo al que se hará referencia más adelante en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="8c776-186">Idealmente, debe guardarlo en el mismo directorio que el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="8c776-187">Por ejemplo, podría llamar a este background.bmp.</span><span class="sxs-lookup"><span data-stu-id="8c776-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="8c776-188">Elija la configuración predeterminada y guarde el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c776-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="8c776-189">El archivo de imagen principal debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="8c776-189">Your primary art file should look like this:</span></span>

![archivo de imagen principal](images/g01prime.png)

<span data-ttu-id="8c776-191">Usará este nombre de archivo como el valor del atributo **BackgroundImage** del elemento **View** en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="8c776-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c776-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c776-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c776-193">**Creación de la primera máscara**</span><span class="sxs-lookup"><span data-stu-id="8c776-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




