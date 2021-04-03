---
title: PPP y Device-Independent píxeles
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Más información acerca de: PPP y Device-Independent píxeles'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913278"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="3ed08-103">PPP y Device-Independent píxeles</span><span class="sxs-lookup"><span data-stu-id="3ed08-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="3ed08-104">Para programar eficazmente con gráficos de Windows, debe comprender dos conceptos relacionados:</span><span class="sxs-lookup"><span data-stu-id="3ed08-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="3ed08-105">Puntos por pulgada (PPP)</span><span class="sxs-lookup"><span data-stu-id="3ed08-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="3ed08-106">Píxeles independientes del dispositivo (DIP).</span><span class="sxs-lookup"><span data-stu-id="3ed08-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="3ed08-107">Comencemos con el reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-107">Let's start with DPI.</span></span> <span data-ttu-id="3ed08-108">Esto requerirá un breve desvío en la tipografía.</span><span class="sxs-lookup"><span data-stu-id="3ed08-108">This will require a short detour into typography.</span></span> <span data-ttu-id="3ed08-109">En la tipografía, el tamaño del tipo se mide en unidades denominadas *puntos*.</span><span class="sxs-lookup"><span data-stu-id="3ed08-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="3ed08-110">Un punto es igual a 1/72 de una pulgada.</span><span class="sxs-lookup"><span data-stu-id="3ed08-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="3ed08-111">1 PT = 1/72 pulgadas</span><span class="sxs-lookup"><span data-stu-id="3ed08-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="3ed08-112">Esta es la definición de publicación de escritorio de Point.</span><span class="sxs-lookup"><span data-stu-id="3ed08-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="3ed08-113">Históricamente, la medida exacta de un punto ha variado.</span><span class="sxs-lookup"><span data-stu-id="3ed08-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="3ed08-114">Por ejemplo, una fuente de 12 puntos está diseñada para caber dentro de una línea de texto 1/6 "(12/72).</span><span class="sxs-lookup"><span data-stu-id="3ed08-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="3ed08-115">Obviamente, esto no significa que todos los caracteres de la fuente tengan exactamente 1/6 "de alto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="3ed08-116">De hecho, algunos caracteres pueden ser más altos que 1/6 ".</span><span class="sxs-lookup"><span data-stu-id="3ed08-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="3ed08-117">Por ejemplo, en muchas fuentes el carácter Å es más alto que el alto nominal de la fuente.</span><span class="sxs-lookup"><span data-stu-id="3ed08-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="3ed08-118">Para que se muestre correctamente, la fuente necesita espacio adicional entre el texto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="3ed08-119">Este espacio se denomina *inicial*.</span><span class="sxs-lookup"><span data-stu-id="3ed08-119">This space is called the *leading*.</span></span>

<span data-ttu-id="3ed08-120">En la ilustración siguiente se muestra una fuente de 72 puntos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="3ed08-121">Las líneas sólidas muestran un cuadro de límite de 1 "en torno al texto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="3ed08-122">La línea discontinua se denomina línea de *base*.</span><span class="sxs-lookup"><span data-stu-id="3ed08-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="3ed08-123">La mayoría de los caracteres de una fuente en reposo en la línea de base.</span><span class="sxs-lookup"><span data-stu-id="3ed08-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="3ed08-124">El alto de la fuente incluye la parte sobre la línea de base (el *ascenso*) y la parte debajo de la línea de base (el *descenso*).</span><span class="sxs-lookup"><span data-stu-id="3ed08-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="3ed08-125">En la fuente que se muestra aquí, el ascenso es 56 puntos y el descenso es de 16 puntos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![Ilustración que muestra una fuente de 72 puntos.](images/graphics11.png)

<span data-ttu-id="3ed08-127">No obstante, cuando se trata de una pantalla de equipo, la medición del tamaño del texto es problemática, ya que los píxeles no tienen el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="3ed08-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="3ed08-128">El tamaño de un píxel depende de dos factores: la resolución de la pantalla y el tamaño físico del monitor.</span><span class="sxs-lookup"><span data-stu-id="3ed08-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="3ed08-129">Por lo tanto, las pulgadas físicas no son una medida útil, ya que no hay ninguna relación fija entre las pulgadas físicas y los píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="3ed08-130">En su lugar, las fuentes se miden en unidades *lógicas* .</span><span class="sxs-lookup"><span data-stu-id="3ed08-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="3ed08-131">Se define una fuente de 72 puntos como una pulgada lógica de alto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="3ed08-132">A continuación, las pulgadas lógicas se convierten en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="3ed08-133">Durante muchos años, Windows usaba la siguiente conversión: una pulgada lógica es igual a 96 píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="3ed08-134">Con este factor de escala, una fuente de 72 puntos se representa como 96 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="3ed08-135">Una fuente de 12 puntos tiene 16 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="3ed08-136">12 puntos = 12/72 de pulgada lógica = 1/6 de pulgada lógica = 96/6 píxeles = 16 píxeles</span><span class="sxs-lookup"><span data-stu-id="3ed08-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="3ed08-137">Este factor de escala se describe como 96 puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="3ed08-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="3ed08-138">El término puntos se deriva de la impresión, donde los puntos de tinta físicos se colocan en el papel.</span><span class="sxs-lookup"><span data-stu-id="3ed08-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="3ed08-139">En el caso de las pantallas de equipo, sería más preciso decir 96 píxeles por pulgada lógica, pero el término DPI se ha atascado.</span><span class="sxs-lookup"><span data-stu-id="3ed08-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="3ed08-140">Dado que los tamaños de píxeles reales varían, el texto que se puede leer en un monitor podría ser demasiado pequeño en otro monitor.</span><span class="sxs-lookup"><span data-stu-id="3ed08-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="3ed08-141">Además, las personas tienen preferencias diferentes; algunas personas prefieren texto más grande.</span><span class="sxs-lookup"><span data-stu-id="3ed08-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="3ed08-142">Por esta razón, Windows permite al usuario cambiar la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="3ed08-143">Por ejemplo, si el usuario establece la presentación en 144 ppp, una fuente de 72 puntos es de 144 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="3ed08-144">La configuración de PPP estándar es 100% (96 PPP), 125% (120 ppp) y 150% (144 ppp).</span><span class="sxs-lookup"><span data-stu-id="3ed08-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="3ed08-145">El usuario también puede aplicar una configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="3ed08-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="3ed08-146">A partir de Windows 7, DPI es una configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="3ed08-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="3ed08-147">Escala de DWM</span><span class="sxs-lookup"><span data-stu-id="3ed08-147">DWM Scaling</span></span>

<span data-ttu-id="3ed08-148">Si un programa no tiene en cuenta el valor de PPP, los siguientes defectos podrían ser obvios con valores altos de PPP:</span><span class="sxs-lookup"><span data-stu-id="3ed08-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="3ed08-149">Elementos de interfaz de usuario recortados.</span><span class="sxs-lookup"><span data-stu-id="3ed08-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="3ed08-150">Diseño incorrecto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-150">Incorrect layout.</span></span>
-   <span data-ttu-id="3ed08-151">Mapas de bits e iconos de Pixelizar.</span><span class="sxs-lookup"><span data-stu-id="3ed08-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="3ed08-152">Coordenadas del mouse incorrectas, que pueden afectar a la prueba de posicionamiento, arrastrar y colocar, etc.</span><span class="sxs-lookup"><span data-stu-id="3ed08-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="3ed08-153">Para asegurarse de que los programas más antiguos funcionan con valores altos de PPP, el DWM implementa una reserva útil.</span><span class="sxs-lookup"><span data-stu-id="3ed08-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="3ed08-154">Si un programa no está marcado como compatible con PPP, el DWM escalará toda la interfaz de usuario para que coincida con la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="3ed08-155">Por ejemplo, a 144 ppp, la interfaz de usuario se escala mediante el 150%, incluidos el texto, los gráficos, los controles y los tamaños de las ventanas.</span><span class="sxs-lookup"><span data-stu-id="3ed08-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="3ed08-156">Si el programa crea una ventana de 500 × 500, la ventana aparece realmente como 750 × 750 píxeles y el contenido de la ventana se escala en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="3ed08-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="3ed08-157">Este comportamiento significa que los programas más antiguos "solo funcionan" con valores altos de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="3ed08-158">Sin embargo, el escalado también da lugar a una apariencia ligeramente borrosa, ya que el escalado se aplica después de que se dibuje la ventana.</span><span class="sxs-lookup"><span data-stu-id="3ed08-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="3ed08-159">Aplicaciones DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="3ed08-159">DPI-Aware Applications</span></span>

<span data-ttu-id="3ed08-160">Para evitar el escalado de DWM, un programa puede marcarse como compatible con PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="3ed08-161">Esto indica a DWM que no realice ninguna escala de PPP automática.</span><span class="sxs-lookup"><span data-stu-id="3ed08-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="3ed08-162">Todas las aplicaciones nuevas deben diseñarse para que sean compatibles con PPP, ya que el reconocimiento de PPP mejora la apariencia de la interfaz de usuario con una configuración de PPP superior.</span><span class="sxs-lookup"><span data-stu-id="3ed08-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="3ed08-163">Un programa se declara a sí mismo a través de su manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ed08-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="3ed08-164">Un *manifiesto* es simplemente un archivo XML que describe una DLL o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ed08-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="3ed08-165">El manifiesto normalmente se incrusta en el archivo ejecutable, aunque se puede proporcionar como un archivo independiente.</span><span class="sxs-lookup"><span data-stu-id="3ed08-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="3ed08-166">Un manifiesto contiene información como las dependencias de DLL, el nivel de privilegios solicitado y la versión de Windows para la que se diseñó el programa.</span><span class="sxs-lookup"><span data-stu-id="3ed08-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="3ed08-167">Para declarar que el programa es compatible con PPP, incluya la siguiente información en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="3ed08-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="3ed08-168">La lista mostrada aquí es solo un manifiesto parcial, pero el enlazador de Visual Studio genera el resto del manifiesto automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3ed08-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="3ed08-169">Para incluir un manifiesto parcial en el proyecto, realice los pasos siguientes en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ed08-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="3ed08-170">En el menú **proyecto** , haga clic en **propiedad**.</span><span class="sxs-lookup"><span data-stu-id="3ed08-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="3ed08-171">En el panel izquierdo, expanda **propiedades de configuración**, expanda la **herramienta manifiesto** y, a continuación, haga clic en **entrada y salida**.</span><span class="sxs-lookup"><span data-stu-id="3ed08-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="3ed08-172">En el cuadro de texto **archivos de manifiesto adicionales** , escriba el nombre del archivo de manifiesto y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3ed08-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="3ed08-173">Al marcar el programa como compatible con PPP, está indicando al DWM que no escale la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ed08-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="3ed08-174">Ahora, si crea una ventana de 500 × 500, la ventana ocupará 500 × 500 píxeles, independientemente del valor de PPP del usuario.</span><span class="sxs-lookup"><span data-stu-id="3ed08-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="3ed08-175">GDI y PPP</span><span class="sxs-lookup"><span data-stu-id="3ed08-175">GDI and DPI</span></span>

<span data-ttu-id="3ed08-176">El dibujo de GDI se mide en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="3ed08-177">Esto significa que si el programa está marcado como compatible con PPP y solicita a GDI que dibuje un rectángulo de 200 × 100, el rectángulo resultante tendrá un ancho de 200 píxeles y 100 píxeles de alto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3ed08-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="3ed08-178">Sin embargo, los tamaños de fuente de GDI se escalan a la configuración de PPP actual.</span><span class="sxs-lookup"><span data-stu-id="3ed08-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="3ed08-179">En otras palabras, si crea una fuente de 72 puntos, el tamaño de la fuente será de 96 píxeles a 96 PPP, pero de 144 píxeles a 144 ppp.</span><span class="sxs-lookup"><span data-stu-id="3ed08-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="3ed08-180">Esta es una fuente de 72 puntos representada a 144 ppp mediante GDI.</span><span class="sxs-lookup"><span data-stu-id="3ed08-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![diagrama que muestra el ajuste de escala de PPP en GDI.](images/graphics12.png)

<span data-ttu-id="3ed08-182">Si la aplicación es compatible con PPP y usa GDI para dibujar, escale todas las coordenadas del dibujo para que coincidan con los ppp.</span><span class="sxs-lookup"><span data-stu-id="3ed08-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="3ed08-183">Direct2D y PPP</span><span class="sxs-lookup"><span data-stu-id="3ed08-183">Direct2D and DPI</span></span>

<span data-ttu-id="3ed08-184">Direct2D realiza el escalado de forma automática para que coincida con la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="3ed08-185">En Direct2D, las coordenadas se miden en unidades denominadas *píxeles independientes del dispositivo* (DIP).</span><span class="sxs-lookup"><span data-stu-id="3ed08-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="3ed08-186">Una DIP se define como 1/1/96 de una pulgada *lógica* .</span><span class="sxs-lookup"><span data-stu-id="3ed08-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="3ed08-187">En Direct2D, todas las operaciones de dibujo se especifican en DIP y luego se escalan a la configuración de PPP actual.</span><span class="sxs-lookup"><span data-stu-id="3ed08-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="3ed08-188">Configuración de PPP</span><span class="sxs-lookup"><span data-stu-id="3ed08-188">DPI setting</span></span> | <span data-ttu-id="3ed08-189">Tamaño de DIP</span><span class="sxs-lookup"><span data-stu-id="3ed08-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="3ed08-190">96</span><span class="sxs-lookup"><span data-stu-id="3ed08-190">96</span></span>          | <span data-ttu-id="3ed08-191">1 píxel</span><span class="sxs-lookup"><span data-stu-id="3ed08-191">1 pixel</span></span>     |
| <span data-ttu-id="3ed08-192">120</span><span class="sxs-lookup"><span data-stu-id="3ed08-192">120</span></span>         | <span data-ttu-id="3ed08-193">1,25 píxeles</span><span class="sxs-lookup"><span data-stu-id="3ed08-193">1.25 pixels</span></span> |
| <span data-ttu-id="3ed08-194">144</span><span class="sxs-lookup"><span data-stu-id="3ed08-194">144</span></span>         | <span data-ttu-id="3ed08-195">1,5 píxeles</span><span class="sxs-lookup"><span data-stu-id="3ed08-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="3ed08-196">Por ejemplo, si la configuración de PPP del usuario es 144 ppp y pide a Direct2D que dibuje un rectángulo de 200 × 100, el rectángulo será de 300 × 150 píxeles físicos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="3ed08-197">Además, DirectWrite mide tamaños de fuente en DIP, en lugar de puntos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="3ed08-198">Para crear una fuente de 12 puntos, especifique 16 DIP (12 puntos = 1/6 Logical pulgada = 96/6 DIP).</span><span class="sxs-lookup"><span data-stu-id="3ed08-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="3ed08-199">Cuando el texto se dibuja en la pantalla, Direct2D convierte los DIP en píxeles físicos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="3ed08-200">La ventaja de este sistema es que las unidades de medida son coherentes tanto para el texto como para el dibujo, independientemente del valor de PPP actual.</span><span class="sxs-lookup"><span data-stu-id="3ed08-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="3ed08-201">Una palabra de PRECAUCIÓN: las coordenadas del mouse y de la ventana todavía se proporcionan en píxeles físicos, no en los DIP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="3ed08-202">Por ejemplo, si procesa el mensaje [**de \_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) , la posición del puntero del mouse se proporciona en píxeles físicos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="3ed08-203">Para dibujar un punto en esa posición, debe convertir las coordenadas de píxel en DIP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="3ed08-204">Convertir píxeles físicos en DIP</span><span class="sxs-lookup"><span data-stu-id="3ed08-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="3ed08-205">La conversión de píxeles físicos a DIP utiliza la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ed08-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="3ed08-206">DIP = píxeles/(DPI/96.0)</span><span class="sxs-lookup"><span data-stu-id="3ed08-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="3ed08-207">Para obtener la configuración de PPP, llame al método [**ID2D1Factory:: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="3ed08-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="3ed08-208">El valor de PPP se devuelve como dos valores de punto flotante, uno para el eje x y otro para el eje y.</span><span class="sxs-lookup"><span data-stu-id="3ed08-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="3ed08-209">En teoría, estos valores pueden ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="3ed08-209">In theory, these values can differ.</span></span> <span data-ttu-id="3ed08-210">Calcular un factor de escala independiente para cada eje.</span><span class="sxs-lookup"><span data-stu-id="3ed08-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="3ed08-211">Esta es una manera alternativa de obtener la configuración de PPP si no está usando Direct2D:</span><span class="sxs-lookup"><span data-stu-id="3ed08-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="3ed08-212">En Windows 10, la versión 1903,  [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) está en desuso y la recomendación es [**DisplayInformation:: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) para aplicaciones de la tienda Windows o [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) para aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3ed08-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="3ed08-213">Si aún desea usarlo, suprima el mensaje de error del compilador escribiendo la línea [**#pragma ADVERTENCIA (suprimir: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) justo antes de la llamada a [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="3ed08-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="3ed08-214">Aunque no se recomienda, es posible establecer el reconocimiento de PPP predeterminado mediante programación con [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span><span class="sxs-lookup"><span data-stu-id="3ed08-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="3ed08-215">Una vez que se ha creado una ventana (HWND) en el proceso, ya no se admite el cambio del modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="3ed08-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="3ed08-216">Si está configurando el modo de reconocimiento de PPP predeterminado del proceso mediante programación, debe llamar a la API correspondiente antes de que se haya creado cualquier HWND.</span><span class="sxs-lookup"><span data-stu-id="3ed08-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="3ed08-217">Para obtener información, consulte [establecer el reconocimiento de PPP predeterminado para un proceso](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="3ed08-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="3ed08-218">Cambiar el tamaño del destino de representación</span><span class="sxs-lookup"><span data-stu-id="3ed08-218">Resizing the Render Target</span></span>

<span data-ttu-id="3ed08-219">Si cambia el tamaño de la ventana, debe cambiar el tamaño del destino de representación para que coincida.</span><span class="sxs-lookup"><span data-stu-id="3ed08-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="3ed08-220">En la mayoría de los casos, también tendrá que actualizar el diseño y volver a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="3ed08-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="3ed08-221">En el código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="3ed08-222">La función [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) obtiene el nuevo tamaño del área cliente, en píxeles físicos (no DIP).</span><span class="sxs-lookup"><span data-stu-id="3ed08-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="3ed08-223">El método [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) actualiza el tamaño del destino de representación, también especificado en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="3ed08-224">La función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) obliga a que se vuelva a dibujar agregando el área de cliente completa a la región de actualización de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3ed08-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="3ed08-225">(Vea [pintar la ventana](painting-the-window.md), en el módulo 1).</span><span class="sxs-lookup"><span data-stu-id="3ed08-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="3ed08-226">A medida que crece o se reduce la ventana, normalmente necesitará volver a calcular la posición de los objetos que dibuje.</span><span class="sxs-lookup"><span data-stu-id="3ed08-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="3ed08-227">Por ejemplo, en el programa Circle, el radio y el punto central deben actualizarse:</span><span class="sxs-lookup"><span data-stu-id="3ed08-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="3ed08-228">El método [**ID2D1RenderTarget::FUL**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) devuelve el tamaño del destino de representación en DIP (no en píxeles), que es la unidad adecuada para calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="3ed08-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="3ed08-229">Hay un método estrechamente relacionado, [**ID2D1RenderTarget:: GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), que devuelve el tamaño en píxeles físicos.</span><span class="sxs-lookup"><span data-stu-id="3ed08-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="3ed08-230">Para un destino de representación de **hWnd** , este valor coincide con el tamaño devuelto por [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span><span class="sxs-lookup"><span data-stu-id="3ed08-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="3ed08-231">Pero recuerde que el dibujo se realiza en DIP, no en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ed08-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="3ed08-232">Siguientes</span><span class="sxs-lookup"><span data-stu-id="3ed08-232">Next</span></span>

[<span data-ttu-id="3ed08-233">Usar el color en Direct2D</span><span class="sxs-lookup"><span data-stu-id="3ed08-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
