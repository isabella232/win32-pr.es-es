---
title: Glosario DirectComposition
description: En este tema se definen los términos de Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359117"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="b5fb0-103">Glosario DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b5fb0-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="b5fb0-104">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="b5fb0-105">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="b5fb0-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="b5fb0-106">En este tema se definen los términos de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="b5fb0-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**función Animation**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-108">Una construcción que especifica cómo cambia el valor de una propiedad de objeto única en un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objeto Animation**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-110">Objeto que representa una función para animar las propiedades de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento de animación**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-112">Definiciones de tiempo fundamentales de una función de animación; son los primitivos de los que se compilan funciones de animación más complejas y de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**búfer de reserva**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-114">Un rectángulo de memoria en el que puede escribir una aplicación directamente.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="b5fb0-115">El búfer de reserva nunca se muestra directamente en el monitor.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**procesamiento**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-117">Grupo de llamadas al método DirectComposition que se procesan de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**myBitmap**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-119">Un búfer de color, ya sea con o sin canal alfa, que reside en la memoria del sistema o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modo de borde**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-121">Propiedad de un visual DirectComposition de Microsoft que afecta al modo en que se componen los bordes de un mapa de bits cuando el mapa de bits se transforma de modo que los bordes no estén alineados por ejes con coordenadas de entero.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="b5fb0-122">También afecta al modo en que el contenido se recorta en las esquinas de un clip con esquinas redondeadas y en el borde de un clip que se transforma de modo que los bordes no estén alineados por ejes con coordenadas de entero.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip (objeto)**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-124">Objeto que representa un rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**rectángulo de recorte**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-126">Conjunto de coordenadas que definen el área del contenido del mapa de bits de visual que se dibuja en la pantalla cuando se representa el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**posibilidad**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-128">Para impedir temporalmente que Administrador de ventanas de escritorio (DWM) dibuje una ventana en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="b5fb0-129">Las aplicaciones normalmente ocultan una ventana mientras que DirectComposition usa el mapa de bits de la ventana en una composición.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**promete**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-131">Para enviar un lote de comandos a DirectCompositionDirectComposition para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modo compuesto**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-133">Una de las distintas formas de mezclar dos mapas de bits (un origen y un destino) para lograr un efecto determinado.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Boletin**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-135">Colección de mapas de bits que se combinan y se manipulan aplicando varias transformaciones, efectos y animaciones para generar un resultado visual deseado en una interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**ventana de destino de composición**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-137">Ventana a la que está enlazado un árbol visual y en la que se dibuja la composición resultante.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**realizado**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-139">Operación que modifica cómo se rasterizan los mapas de bits de un árbol visual, normalmente aplicando un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Grupo de efectos**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-141">Grupo de efectos de imagen que se aplican conjuntamente para modificar la rasterización del subárbol de un objeto visual.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**grama**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-143">Iteración del motor de composición que genera una rasterización del árbol visual.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**búfer frontal**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-145">Un rectángulo de memoria que el adaptador de gráficos traduce y que se muestra en el monitor.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modo de interpolación**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-147">Propiedad que determina cómo se crea un mapa de bits cuando se transforma de modo que no hay una correspondencia uno a uno entre los píxeles del mapa de bits y los píxeles de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**raíz visual**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-149">El visual del que todos los demás objetos visuales de un árbol visual son descendentes.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-151">Colección de uno o más búferes de reserva que se pueden presentar en serie al búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**Calcomanía**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-153">Representación de un área lineal de memoria de presentación que normalmente reside en la memoria de visualización de la tarjeta de presentación, aunque pueden existir superficies en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transformación**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-155">Matriz que representa una transformación de coordenadas en un espacio bidimensional o tridimensional.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transformar grupo**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-157">Colección de transformaciones cuyas matrices se multiplican juntas en el orden en que se especifican en la colección antes de que se apliquen a un objeto visual.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-159">Objeto que contiene una referencia opcional a un objeto de mapa de bits y un conjunto de propiedades que determinan dónde y cómo se representa el mapa de bits en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objeto visual**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-161">Vea [*Visual*](/windows).</span><span class="sxs-lookup"><span data-stu-id="b5fb0-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**subárbol visual**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-163">Una parte de un árbol visual que se compone de un elemento visual determinado y de todos sus objetos visuales secundarios y descendientes.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**árbol visual**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-165">Colección jerárquica de objetos visuales que se usan para crear una composición.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="b5fb0-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**cadena de intercambio sin ventanas**</span><span class="sxs-lookup"><span data-stu-id="b5fb0-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="b5fb0-167">Cadena de intercambio que está asociada a un objeto visual DirectComposition en lugar de a una ventana.</span><span class="sxs-lookup"><span data-stu-id="b5fb0-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 