---
title: Especificar recursos de imagen de cinta
description: Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones de Windows está diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta. Todos los recursos de imagen se declaran en el marcado de la cinta o se consultan desde una aplicación host de cinta.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Cinta de Windows, recursos de imagen
- Cinta, recursos de imagen
- Cinta de Windows, transparencia
- Cinta de opciones, transparencia
- Cinta de Windows, profundidad de color
- Cinta, profundidad de color
- Cinta de opciones de Windows, contraste
- Cinta, contraste
- recursos de imagen en la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488123"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="57e46-113">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="57e46-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="57e46-114">Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones de Windows está diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta.</span><span class="sxs-lookup"><span data-stu-id="57e46-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="57e46-115">Todos los recursos de imagen se declaran en el [marcado de la cinta](windowsribbon-schema.md) o se consultan desde una aplicación host de cinta.</span><span class="sxs-lookup"><span data-stu-id="57e46-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="57e46-116">En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.</span><span class="sxs-lookup"><span data-stu-id="57e46-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="57e46-117">En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.</span><span class="sxs-lookup"><span data-stu-id="57e46-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="57e46-118">Puede producirse un error de compilación si se proporciona un formato de imagen no compatible al marco.</span><span class="sxs-lookup"><span data-stu-id="57e46-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="57e46-119">Tamaños de imagen</span><span class="sxs-lookup"><span data-stu-id="57e46-119">Image Sizes</span></span>

<span data-ttu-id="57e46-120">Para proporcionar mayor flexibilidad a los diseños de controles de la cinta al cambiar el tamaño de una ventana de la aplicación, el marco de cinta acepta y representa imágenes en uno de dos tamaños: grande o pequeño.</span><span class="sxs-lookup"><span data-stu-id="57e46-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="57e46-121">Las siguientes imágenes ilustran una aplicación de cinta que admite varios tamaños de cinta a través de diseños de control flexibles y la sustitución de imágenes grandes con imágenes pequeñas cuando están disponibles.</span><span class="sxs-lookup"><span data-stu-id="57e46-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="57e46-122">En la captura de pantalla siguiente se muestra la cinta de opciones con imágenes grandes para los controles de zoom.</span><span class="sxs-lookup"><span data-stu-id="57e46-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![captura de pantalla que muestra una cinta que usa imágenes grandes para los controles de zoom.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="57e46-124">En la captura de pantalla siguiente se muestra la misma cinta cuyo tamaño se ha cambiado con imágenes pequeñas para los controles de zoom</span><span class="sxs-lookup"><span data-stu-id="57e46-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![captura de pantalla que muestra una cinta que usa imágenes pequeñas para los controles de zoom.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="57e46-126">En la captura de pantalla siguiente se muestra la cinta de opciones en estado oculto.</span><span class="sxs-lookup"><span data-stu-id="57e46-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="57e46-127">La cinta de opciones se oculta cuando se han agotado todos los diseños de control potenciales y la cinta de opciones no se puede representar con un área de trabajo de aplicación utilizable.</span><span class="sxs-lookup"><span data-stu-id="57e46-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![captura de pantalla que muestra una cinta contraída.](images/overviews/imageresources-noimage.png)

<span data-ttu-id="57e46-129">En cualquier imagen, el tamaño exacto en píxeles depende de la resolución de la pantalla, o de puntos por pulgada (PPP), del monitor que se está usando.</span><span class="sxs-lookup"><span data-stu-id="57e46-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="57e46-130">En 96 PPP, las imágenes grandes tienen un tamaño de 32 x 32 píxeles y las imágenes pequeñas son de 16 x 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="57e46-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="57e46-131">Los tamaños de imagen aumentan de manera lineal en relación con los PPP, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="57e46-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="57e46-132">ppp</span><span class="sxs-lookup"><span data-stu-id="57e46-132">DPI</span></span>     | <span data-ttu-id="57e46-133">Imagen pequeña</span><span class="sxs-lookup"><span data-stu-id="57e46-133">Small Image</span></span>  | <span data-ttu-id="57e46-134">Imagen grande</span><span class="sxs-lookup"><span data-stu-id="57e46-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="57e46-135">96 PPP</span><span class="sxs-lookup"><span data-stu-id="57e46-135">96 dpi</span></span>  | <span data-ttu-id="57e46-136">16x16 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-136">16x16 pixels</span></span> | <span data-ttu-id="57e46-137">32x32 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-137">32x32 pixels</span></span> |
| <span data-ttu-id="57e46-138">120 ppp</span><span class="sxs-lookup"><span data-stu-id="57e46-138">120 dpi</span></span> | <span data-ttu-id="57e46-139">20x20 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-139">20x20 pixels</span></span> | <span data-ttu-id="57e46-140">40 x 40 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-140">40x40 pixels</span></span> |
| <span data-ttu-id="57e46-141">144 ppp</span><span class="sxs-lookup"><span data-stu-id="57e46-141">144 dpi</span></span> | <span data-ttu-id="57e46-142">24x24 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-142">24x24 pixels</span></span> | <span data-ttu-id="57e46-143">48x48 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-143">48x48 pixels</span></span> |
| <span data-ttu-id="57e46-144">192 PPP</span><span class="sxs-lookup"><span data-stu-id="57e46-144">192 dpi</span></span> | <span data-ttu-id="57e46-145">32x32 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-145">32x32 pixels</span></span> | <span data-ttu-id="57e46-146">64 x 64 píxeles</span><span class="sxs-lookup"><span data-stu-id="57e46-146">64x64 pixels</span></span> |



 

<span data-ttu-id="57e46-147">El marco de cinta escala los recursos de imagen según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="57e46-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="57e46-148">Sin embargo, dado que el cambio de tamaño puede producir artefactos no deseados y degradación de la imagen, se recomienda encarecidamente que la aplicación proporcione un pequeño conjunto de recursos de imagen que abarquen varios valores de PPP usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="57e46-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="57e46-149">Si no se encuentra una coincidencia exacta, la imagen más cercana se escalará o reducirá verticalmente.</span><span class="sxs-lookup"><span data-stu-id="57e46-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="57e46-150">Para facilitar esto, los recursos de imagen se pueden declarar en el marcado de la cinta de opciones mediante un conjunto de elementos [**Image**](windowsribbon-element-image.md) para cada elemento [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="57e46-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="57e46-151">En tiempo de ejecución, el marco de trabajo selecciona la imagen que se va a mostrar basándose en el atributo *MinDPI* de cada elemento de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="57e46-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="57e46-152">Cuando se proporciona una colección de recursos de imagen que están diseñados para admitir valores de PPP de pantalla específicos para el marco de cinta a través de un conjunto de elementos de [**imagen**](windowsribbon-element-image.md) , el marco de trabajo usa la **imagen** con un valor de atributo *MinDPI* que coincide con la configuración de PPP de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="57e46-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="57e46-153">Si no se declara ningún elemento de [**imagen**](windowsribbon-element-image.md) con un valor de *MinDPI* que coincida con la configuración de PPP de pantalla actual, el marco de trabajo selecciona la **imagen** que tiene el valor de *MinDPI* más cercano menor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="57e46-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="57e46-154">De lo contrario, si no se declara ningún elemento de **imagen** con un valor de atributo *MinDPI* inferior al valor de PPP de pantalla actual, el marco de trabajo selecciona el valor de *MinDPI* más cercano mayor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="57e46-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="57e46-155">En el ejemplo siguiente se muestra cómo declarar un conjunto de imágenes para acomodar varios tamaños de cinta y configuraciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="57e46-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="57e46-156">Si las imágenes declaradas en el marcado se invalidan en tiempo de ejecución por cualquier motivo, se consultan las nuevas imágenes de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="57e46-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="57e46-157">Cuando estas imágenes se generan y se cargan mediante programación, la aplicación debe intentar devolver imágenes cuyo tamaño se ajusta a los tamaños de icono del sistema predeterminados determinados por la [ \_ métrica del sistema SM CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span><span class="sxs-lookup"><span data-stu-id="57e46-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="57e46-158">Las imágenes grandes tienen un tamaño de SM \_ CXICON por SM \_ CXICON y las imágenes pequeñas tienen un tamaño de SM \_ CXICON/2 por SM \_ CXICON/2.</span><span class="sxs-lookup"><span data-stu-id="57e46-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="57e46-159">Profundidad de color, transparencia y contraste</span><span class="sxs-lookup"><span data-stu-id="57e46-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="57e46-160">Se espera que las imágenes normales tengan el formato de píxel ARGB de 32 bits por píxel (BPP) y que se escalen al tamaño del icono del sistema predeterminado.</span><span class="sxs-lookup"><span data-stu-id="57e46-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="57e46-161">Este formato admite la transparencia y el suavizado de contorno (usando 8 bits por canal).</span><span class="sxs-lookup"><span data-stu-id="57e46-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="57e46-162">Muchas herramientas de edición de imágenes no conservan el canal alfa de 8 bits de orden superior al cargar o guardar imágenes de 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="57e46-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="57e46-163">Para que una imagen se muestre correctamente en el modo de contraste alto, debe tener un formato de píxel de 4 BPP con un formato de píxeles.</span><span class="sxs-lookup"><span data-stu-id="57e46-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="57e46-164">Cuando se representa la imagen, el marco de la cinta de opciones reasigna los colores específicos en función del contexto de alto contraste de la imagen.</span><span class="sxs-lookup"><span data-stu-id="57e46-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="57e46-165">En la tabla siguiente se muestra el comportamiento de representación de color de alto contraste del marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="57e46-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="57e46-166">Color de píxel</span><span class="sxs-lookup"><span data-stu-id="57e46-166">Pixel color</span></span>

<span data-ttu-id="57e46-167">Valor RGB</span><span class="sxs-lookup"><span data-stu-id="57e46-167">RGB value</span></span>

<span data-ttu-id="57e46-168">Comportamiento</span><span class="sxs-lookup"><span data-stu-id="57e46-168">Behavior</span></span>

<span data-ttu-id="57e46-169">Fondo blanco</span><span class="sxs-lookup"><span data-stu-id="57e46-169">White background</span></span>

<span data-ttu-id="57e46-170">Fondo oscuro</span><span class="sxs-lookup"><span data-stu-id="57e46-170">Dark Background</span></span>

<span data-ttu-id="57e46-171">FUCSIA</span><span class="sxs-lookup"><span data-stu-id="57e46-171">MAGENTA</span></span>

<span data-ttu-id="57e46-172">800080</span><span class="sxs-lookup"><span data-stu-id="57e46-172">800080</span></span>

<span data-ttu-id="57e46-173">Transparente</span><span class="sxs-lookup"><span data-stu-id="57e46-173">Transparent</span></span>

<span data-ttu-id="57e46-174">Transparente</span><span class="sxs-lookup"><span data-stu-id="57e46-174">Transparent</span></span>

<span data-ttu-id="57e46-175">BLANCO</span><span class="sxs-lookup"><span data-stu-id="57e46-175">BLACK</span></span>

<span data-ttu-id="57e46-176">000000</span><span class="sxs-lookup"><span data-stu-id="57e46-176">000000</span></span>

<span data-ttu-id="57e46-177">COLOR \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="57e46-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="57e46-178">Blanco</span><span class="sxs-lookup"><span data-stu-id="57e46-178">WHITE</span></span>

<span data-ttu-id="57e46-179">Blanco</span><span class="sxs-lookup"><span data-stu-id="57e46-179">WHITE</span></span>

<span data-ttu-id="57e46-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="57e46-180">FFFFFF</span></span>

<span data-ttu-id="57e46-181">ventana de COLOR \_</span><span class="sxs-lookup"><span data-stu-id="57e46-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="57e46-182">BLANCO</span><span class="sxs-lookup"><span data-stu-id="57e46-182">BLACK</span></span>

<span data-ttu-id="57e46-183">GRIS OSCURO</span><span class="sxs-lookup"><span data-stu-id="57e46-183">DARK GRAY</span></span>

<span data-ttu-id="57e46-184">808080</span><span class="sxs-lookup"><span data-stu-id="57e46-184">808080</span></span>

<span data-ttu-id="57e46-185">COLOR \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="57e46-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="57e46-186">COLOR \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="57e46-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="57e46-187">AMBIGUO</span><span class="sxs-lookup"><span data-stu-id="57e46-187">GRAY</span></span>

<span data-ttu-id="57e46-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="57e46-188">C0C0C0</span></span>

<span data-ttu-id="57e46-189">COLOR \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="57e46-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="57e46-190">COLOR \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="57e46-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="57e46-191">GRIS CLARO</span><span class="sxs-lookup"><span data-stu-id="57e46-191">LIGHT GRAY</span></span>

<span data-ttu-id="57e46-192">DFDFDF</span><span class="sxs-lookup"><span data-stu-id="57e46-192">DFDFDF</span></span>

<span data-ttu-id="57e46-193">COLOR \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="57e46-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="57e46-194">COLOR \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="57e46-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="57e46-195">AZUL MARINO</span><span class="sxs-lookup"><span data-stu-id="57e46-195">DARK BLUE</span></span>

<span data-ttu-id="57e46-196">000080</span><span class="sxs-lookup"><span data-stu-id="57e46-196">000080</span></span>

<span data-ttu-id="57e46-197">N/D</span><span class="sxs-lookup"><span data-stu-id="57e46-197">n/a</span></span>

<span data-ttu-id="57e46-198">Blanco</span><span class="sxs-lookup"><span data-stu-id="57e46-198">WHITE</span></span>



 

<span data-ttu-id="57e46-199">Para obtener más información sobre los formatos de imagen admitidos por el marco de la cinta de opciones, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57e46-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="57e46-200">[Estructura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) : describe el formato de píxel ARGB 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="57e46-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="57e46-201">[Función CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) : describe cómo crear una imagen de formato de píxel ARGB de 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="57e46-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="57e46-202">[Función LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) : describe cómo cargar una imagen de formato de píxel ARGB 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="57e46-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="57e46-203">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="57e46-203">Accessibility</span></span>

<span data-ttu-id="57e46-204">Basándose en los recursos de imagen para proporcionar información, transmitir la funcionalidad de control y exponer el estado de la aplicación, aumenta la necesidad de los requisitos de accesibilidad durante el desarrollo y el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="57e46-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="57e46-205">En el caso de la compatibilidad básica de contraste alto, la cinta permite que se muestre un conjunto independiente de archivos de imagen cuando un tema de contraste alto está activo.</span><span class="sxs-lookup"><span data-stu-id="57e46-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="57e46-206">Estas imágenes pueden ser de 32 BPP o 4 BPP, con colores asignados a una paleta especial en la que se invierten los colores oscuros y claros en función de los colores de primer plano y de fondo del tema activo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="57e46-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="57e46-207">En el ejemplo siguiente se muestra cómo se declaran los recursos de imagen de contraste alto en el marcado de la cinta de opciones:</span><span class="sxs-lookup"><span data-stu-id="57e46-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="57e46-208">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57e46-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e46-209">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="57e46-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="57e46-210">UI \_ PKEY \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="57e46-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="57e46-211">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="57e46-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="57e46-212">UI \_ PKEY \_ LargeImage</span><span class="sxs-lookup"><span data-stu-id="57e46-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="57e46-213">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="57e46-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="57e46-214">UI \_ PKEY \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="57e46-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="57e46-215">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="57e46-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="57e46-216">UI \_ PKEY \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="57e46-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 