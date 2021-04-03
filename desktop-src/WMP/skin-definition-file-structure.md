---
title: Estructura del archivo de definición de máscara
description: Estructura del archivo de definición de máscara
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075989"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="ff1a6-107">Estructura del archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="ff1a6-107">Skin Definition File Structure</span></span>

<span data-ttu-id="ff1a6-108">El archivo de definición de máscara debe seguir una estructura específica.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="ff1a6-109">Empiece con un elemento de **tema** , cree uno o varios elementos de **vista** y, a continuación, defina cada elemento de **vista** con los elementos de la interfaz de usuario adecuados para el tipo de vista que desee usar.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="ff1a6-110">Elementos de tema</span><span class="sxs-lookup"><span data-stu-id="ff1a6-110">THEME Elements</span></span>

<span data-ttu-id="ff1a6-111">En el nivel superior, debe iniciar el archivo de definición de máscara con el elemento de **tema** y cerrar con él.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="ff1a6-112">El elemento **Theme** es el elemento raíz de la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="ff1a6-113">Solo puede haber un elemento de **tema** en un archivo de definición de máscara y debe estar en el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="ff1a6-114">Los elementos de **tema** tienen atributos específicos y de ambiente, aunque la mayoría de las veces no necesitará usarlos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="ff1a6-115">Para obtener más información sobre estos atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="ff1a6-116">Elementos de vista</span><span class="sxs-lookup"><span data-stu-id="ff1a6-116">VIEW Elements</span></span>

<span data-ttu-id="ff1a6-117">Cada **tema** debe tener al menos un elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="ff1a6-118">El elemento de **vista** rige la imagen determinada que se ve en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="ff1a6-119">Puede que desee tener más de una vista, de modo que pueda cambiar de una a otra.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="ff1a6-120">Por ejemplo, puede que desee tener una vista grande para trabajar con listas de reproducción, una vista mediana para ver visualizaciones y una vista pequeña que quepa en una esquina de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="ff1a6-121">Si va a crear varias vistas, querrá asegurarse de que cada vista tiene un valor de atributo de **identificador** único que se utilizará para identificar la vista.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="ff1a6-122">Debe definir el atributo **BackgroundImage** o la vista no tendrá ninguna imagen de inicio.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="ff1a6-123">Si no desea mostrar una imagen rectangular, probablemente querrá usar el atributo **clippingColor** para definir las áreas de la máscara que no se mostrarán, y es probable que desee establecer el atributo **TitleBar** del elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="ff1a6-124">Cada elemento de **vista** también puede tener uno o más elementos de **vista previa** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="ff1a6-125">Un elemento de **subvista** es similar a una **vista** y se puede usar para las partes de la máscara que desea desplazar, ocultar o mostrar.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="ff1a6-126">Por ejemplo, un elemento de una **subvista** podría usarse para crear una bandeja deslizante que extrae de la máscara para mostrar un ecualizador gráfico.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="ff1a6-127">Los elementos de la vista **previa** se pueden alinear con la **vista** y tienen otras relaciones especiales con la **vista**.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="ff1a6-128">Inicializar Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="ff1a6-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="ff1a6-129">Puede establecer ciertas propiedades iniciales de Windows Media Player mediante los elementos **Player**, **Settings** y **Controls** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="ff1a6-130">Por ejemplo, puede establecer el volumen en un nivel inicial o asignar un valor predeterminado a un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="ff1a6-131">En el código siguiente se muestra cómo establecer el valor de la **dirección URL** en una máscara:</span><span class="sxs-lookup"><span data-stu-id="ff1a6-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="ff1a6-132">Si desea establecer el atributo **autoStart** de **Settings** en false, usaría el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff1a6-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="ff1a6-133">Tenga en cuenta que el elemento **Settings** está anidado dentro del elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="ff1a6-134">Con estos elementos, se pueden especificar los siguientes atributos y eventos en tiempo de diseño:</span><span class="sxs-lookup"><span data-stu-id="ff1a6-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="ff1a6-135">**Atributos del elemento PLAYER**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="ff1a6-136">**url**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-136">**url**</span></span>
-   <span data-ttu-id="ff1a6-137">**de respuesta**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-137">**Buffering**</span></span>
-   <span data-ttu-id="ff1a6-138">**Currentitemchange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="ff1a6-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="ff1a6-140">**Error**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-140">**Error**</span></span>
-   <span data-ttu-id="ff1a6-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-141">**Markerhit**</span></span>
-   <span data-ttu-id="ff1a6-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-142">**Mediachange**</span></span>
-   <span data-ttu-id="ff1a6-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="ff1a6-144">**Modechange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-144">**Modechange**</span></span>
-   <span data-ttu-id="ff1a6-145">**Mpenstatechange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="ff1a6-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="ff1a6-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="ff1a6-148">**Mositionchange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-148">**Mositionchange**</span></span>
-   <span data-ttu-id="ff1a6-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="ff1a6-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-150">**Mtatuschange**</span></span>

<span data-ttu-id="ff1a6-151">**Atributos del elemento SETTINGs**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="ff1a6-152">**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-152">**autoStart**</span></span>
-   <span data-ttu-id="ff1a6-153">**balancea**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-153">**balance**</span></span>
-   <span data-ttu-id="ff1a6-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-154">**baseURL**</span></span>
-   <span data-ttu-id="ff1a6-155">**defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-155">**defaultFrame**</span></span>
-   <span data-ttu-id="ff1a6-156">**enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="ff1a6-157">**invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-157">**invokeURLs**</span></span>
-   <span data-ttu-id="ff1a6-158">**silenciar**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-158">**mute**</span></span>
-   <span data-ttu-id="ff1a6-159">**playCount**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-159">**playCount**</span></span>
-   <span data-ttu-id="ff1a6-160">**Rate**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-160">**rate**</span></span>
-   <span data-ttu-id="ff1a6-161">**volume**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="ff1a6-162">Atributos del elemento CONTROLs</span><span class="sxs-lookup"><span data-stu-id="ff1a6-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="ff1a6-163">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-163">**currentMarker**</span></span>
-   <span data-ttu-id="ff1a6-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="ff1a6-165">Otros elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ff1a6-165">Other User Interface Elements</span></span>

<span data-ttu-id="ff1a6-166">Una vez que haya definido los elementos de **vista** y **tema** , debe rellenar la **vista** con elementos específicos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="ff1a6-167">No tiene que utilizar todos los elementos disponibles en una máscara, solo los que necesita.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="ff1a6-168">Si el usuario puede visualizar un elemento, se denomina control.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="ff1a6-169">Los siguientes controles están disponibles para las máscaras:</span><span class="sxs-lookup"><span data-stu-id="ff1a6-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="ff1a6-170">Botones</span><span class="sxs-lookup"><span data-stu-id="ff1a6-170">Buttons</span></span>
-   <span data-ttu-id="ff1a6-171">Controles deslizantes, controles deslizantes personalizados y barras de progreso</span><span class="sxs-lookup"><span data-stu-id="ff1a6-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="ff1a6-172">Cuadros de texto</span><span class="sxs-lookup"><span data-stu-id="ff1a6-172">Text boxes</span></span>
-   <span data-ttu-id="ff1a6-173">Ventanas de vídeo</span><span class="sxs-lookup"><span data-stu-id="ff1a6-173">Video windows</span></span>
-   <span data-ttu-id="ff1a6-174">Ventanas de visualización</span><span class="sxs-lookup"><span data-stu-id="ff1a6-174">Visualization windows</span></span>
-   <span data-ttu-id="ff1a6-175">Ventanas de lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="ff1a6-175">Playlist windows</span></span>
-   <span data-ttu-id="ff1a6-176">Ventanas de subvista</span><span class="sxs-lookup"><span data-stu-id="ff1a6-176">Subview windows</span></span>

<span data-ttu-id="ff1a6-177">Además, se pueden utilizar varios elementos para definir con mayor precisión las acciones de Media Player de Windows, pero requieren elementos visuales como botones o controles deslizantes:</span><span class="sxs-lookup"><span data-stu-id="ff1a6-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="ff1a6-178">Configuración de vídeo</span><span class="sxs-lookup"><span data-stu-id="ff1a6-178">Video settings</span></span>
-   <span data-ttu-id="ff1a6-179">Configuración del ecualizador</span><span class="sxs-lookup"><span data-stu-id="ff1a6-179">Equalizer Settings</span></span>
-   <span data-ttu-id="ff1a6-180">Configuración de visualización</span><span class="sxs-lookup"><span data-stu-id="ff1a6-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="ff1a6-181">Botones</span><span class="sxs-lookup"><span data-stu-id="ff1a6-181">Buttons</span></span>

<span data-ttu-id="ff1a6-182">Los botones son la parte más popular de una máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="ff1a6-183">Puede usar botones para desencadenar acciones como reproducir, detener, salir, minimizar y cambiar a vista diferente.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="ff1a6-184">Windows Media Player proporciona el creador de la máscara con dos tipos de elementos Button: el elemento **Button** y el elemento **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="ff1a6-185">Además, hay varios tipos de botones predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="ff1a6-186">**Elemento BUTTON.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-186">**BUTTON element.**</span></span> <span data-ttu-id="ff1a6-187">El elemento **Button** se usa para botones individuales.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="ff1a6-188">Si usa el elemento de **botón** , debe proporcionar una imagen para cada botón y definir la ubicación exacta en la que desea que aparezca el botón en relación con la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="ff1a6-189">Una de las ventajas del elemento **Button** es que puede cambiar dinámicamente la imagen del botón.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="ff1a6-190">**Elemento BUTTONGROUP.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="ff1a6-191">El elemento **BUTTONGROUP** se usa para grupos de botones.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="ff1a6-192">De hecho, debe incluir cada elemento **BUTTONGROUP** con un par de etiquetas **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="ff1a6-193">El uso de grupos de botones es más fácil que usar botones individuales, ya que no es necesario especificar la ubicación exacta de cada botón.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="ff1a6-194">En su lugar, se proporciona un mapa de imágenes independiente que define las acciones que tendrán lugar cuando se mantenga el mouse sobre un área en el fondo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="ff1a6-195">El uso de mapas de imagen es fácil porque puede tomar el arte que ha creado para el fondo y copiarlo en una capa de asignación en el programa de edición de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="ff1a6-196">Usar el programa de edición de gráficos es más rápido y preciso que intentar definir exactamente dónde se debe colocar un botón individual en el fondo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="ff1a6-197">**Botones predefinidos.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-197">**Predefined buttons.**</span></span> <span data-ttu-id="ff1a6-198">Hay varios botones predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-198">There are several predefined buttons.</span></span> <span data-ttu-id="ff1a6-199">Por ejemplo, puede usar un botón PLAYELEMENT para reproducir archivos multimedia digitales y un STOPELEMENT para detener la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="ff1a6-200">Vea elemento [BUTTONGROUP](buttongroup-element.md) y el [elemento Button](button-element.md) en la referencia de programación de la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="ff1a6-201">El [IMAGEBUTTON](imagebutton.md) se puede usar para mostrar imágenes que pueden cambiar en respuesta a eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="ff1a6-202">Controles deslizantes</span><span class="sxs-lookup"><span data-stu-id="ff1a6-202">Sliders</span></span>

<span data-ttu-id="ff1a6-203">Los controles deslizantes son útiles para trabajar con información que cambia con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="ff1a6-204">Por ejemplo, puede usar un control deslizante para indicar la cantidad de música que ya ha jugado para un archivo multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="ff1a6-205">Los controles deslizantes pueden ser horizontales o verticales, lineales o circulares, o cualquier forma que pueda considerar.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="ff1a6-206">Los controles deslizantes tienen tres variedades: controles deslizantes, barras de progreso y controles deslizantes personalizados.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="ff1a6-207">**Controles deslizantes.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-207">**Sliders.**</span></span> <span data-ttu-id="ff1a6-208">Puede usar el elemento **Slider** para controles de volumen o para permitir que el usuario se mueva a otra parte del contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="ff1a6-209">**Barras de progreso.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-209">**Progress bars.**</span></span> <span data-ttu-id="ff1a6-210">Las barras de progreso son similares a los controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="ff1a6-211">Las barras de progreso están diseñadas para mostrar gráficamente el porcentaje de un proceso determinado que se ha completado, pero no para un proceso con el que el usuario desea interactuar.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="ff1a6-212">Por ejemplo, puede que desee usar una barra de progreso para indicar el progreso del almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="ff1a6-213">**Controles deslizantes personalizados.**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-213">**Custom sliders.**</span></span> <span data-ttu-id="ff1a6-214">Se proporciona funcionalidad de control deslizante personalizado para que pueda crear controles, como botones, o crear mecanismos de control inusuales.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="ff1a6-215">Por ejemplo, si desea crear un control de volumen que se ajuste alrededor de la máscara, puede hacerlo con un control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="ff1a6-216">Para configurar el control deslizante personalizado, debe crear un mapa de imágenes que contenga imágenes de escala de grises para definir las ubicaciones de los valores en el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="ff1a6-217">Esto es relativamente fácil de hacer con un programa de edición de gráficos que admita capas.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="ff1a6-218">Texto</span><span class="sxs-lookup"><span data-stu-id="ff1a6-218">Text</span></span>

<span data-ttu-id="ff1a6-219">Puede usar el elemento de **texto** para mostrar texto en la máscara, como títulos de canciones.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="ff1a6-220">Vídeo</span><span class="sxs-lookup"><span data-stu-id="ff1a6-220">Video</span></span>

<span data-ttu-id="ff1a6-221">Puede mostrar vídeo en la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-221">You can display video in your skin.</span></span> <span data-ttu-id="ff1a6-222">El elemento de **vídeo** le permite establecer el tamaño y la posición de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="ff1a6-223">También puede permitir que el usuario cambie la configuración de vídeo con el elemento de **configuración** de videojuegos.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="ff1a6-224">Por ejemplo, puede crear controles para ajustar el brillo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="ff1a6-225">Si no se proporciona un elemento de vídeo y el contenido contiene vídeo, Windows Media Player volverá al modo completo y no se mostrará la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="ff1a6-226">Configuración del ecualizador</span><span class="sxs-lookup"><span data-stu-id="ff1a6-226">Equalizer Settings</span></span>

<span data-ttu-id="ff1a6-227">Puede establecer el filtrado para bandas de frecuencia de audio específicas mediante el elemento **EQUALIZERSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="ff1a6-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="ff1a6-228">Puede aumentar el valor de graves, retocar el agudo y configurar sus sonidos para que se adapten a sus oídos o a su salón.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="ff1a6-229">Visualizaciones</span><span class="sxs-lookup"><span data-stu-id="ff1a6-229">Visualizations</span></span>

<span data-ttu-id="ff1a6-230">Puede mostrar visualizaciones en la máscara.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="ff1a6-231">Las visualizaciones son efectos visuales que cambian con el tiempo a medida que el audio se reproduce a través de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="ff1a6-232">El elemento **Effects** determina dónde se reproducirán las visualizaciones, el tamaño de la ventana y las visualizaciones que se reproducirán.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="ff1a6-233">Reproducción</span><span class="sxs-lookup"><span data-stu-id="ff1a6-233">Playlists</span></span>

<span data-ttu-id="ff1a6-234">Puede usar el elemento de **lista de reproducción** para permitir que el usuario seleccione un elemento de una lista de reproducción específica.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="ff1a6-235">Subvistas</span><span class="sxs-lookup"><span data-stu-id="ff1a6-235">Subviews</span></span>

<span data-ttu-id="ff1a6-236">Puede utilizar el elemento de la **subvista** para mostrar los conjuntos secundarios de controles de interfaz, como una lista de reproducción o un control de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff1a6-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff1a6-237">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff1a6-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff1a6-238">**Archivos de máscara**</span><span class="sxs-lookup"><span data-stu-id="ff1a6-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




