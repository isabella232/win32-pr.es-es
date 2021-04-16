---
title: Marcos de ventana
description: La mayoría de los programas deben usar marcos de ventana estándar. Las aplicaciones envolventes pueden tener un modo de pantalla completa que oculte el marco de la ventana. Considere la posibilidad de usar cristal estratégicamente para obtener un aspecto más sencillo, más claro y más coherente.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558325"
---
# <a name="window-frames"></a><span data-ttu-id="55992-105">Marcos de ventana</span><span class="sxs-lookup"><span data-stu-id="55992-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="55992-106">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="55992-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="55992-107">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="55992-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="55992-108">La mayoría de los programas deben usar marcos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="55992-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="55992-109">Las aplicaciones envolventes pueden tener un modo de pantalla completa que oculte el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="55992-110">Considere la posibilidad de usar cristal estratégicamente para obtener un aspecto más sencillo, más claro y más coherente.</span><span class="sxs-lookup"><span data-stu-id="55992-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="55992-111">Con un marco de ventana, los usuarios pueden manipular una ventana y ver el título y el icono para identificar su contenido.</span><span class="sxs-lookup"><span data-stu-id="55992-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="55992-112">captura de pantalla del marco de ventana alrededor de la ventana del Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="55992-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="55992-113">Marco de ventana típico.</span><span class="sxs-lookup"><span data-stu-id="55992-113">A typical window frame.</span></span>

<span data-ttu-id="55992-114">**Nota:** Las instrucciones relacionadas con la [Administración de ventanas](win-window-mgt.md) y la [Personalización de marca](exper-branding.md) se presentan en artículos independientes.</span><span class="sxs-lookup"><span data-stu-id="55992-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="55992-115">Conceptos de diseño</span><span class="sxs-lookup"><span data-stu-id="55992-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="55992-116">Cuadros de ventana de cristal</span><span class="sxs-lookup"><span data-stu-id="55992-116">Glass window frames</span></span>

<span data-ttu-id="55992-117">Los marcos de ventana Glass son un nuevo aspecto sorprendente de la estética de Microsoft Windows, con el objetivo de ser atractivos y ligeros.</span><span class="sxs-lookup"><span data-stu-id="55992-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="55992-118">Estos fotogramas translúcidos proporcionan a Windows una apariencia menos intrusiva, que ayuda a los usuarios a centrarse en el contenido y la funcionalidad, en lugar de en la interfaz que lo rodea.</span><span class="sxs-lookup"><span data-stu-id="55992-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="55992-119">captura de pantalla del marco Glass alrededor de la calculadora</span><span class="sxs-lookup"><span data-stu-id="55992-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="55992-120">Marcos de la ventana de cristal.</span><span class="sxs-lookup"><span data-stu-id="55992-120">Glass window frames.</span></span>

<span data-ttu-id="55992-121">Puede usar cristal de manera estratégica en pequeñas regiones dentro de una ventana que toca el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="55992-122">Estas regiones parecen formar parte del marco de ventana, aunque técnicamente forman parte del área de cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="55992-123">captura de pantalla de la ventana con borde translúcido</span><span class="sxs-lookup"><span data-stu-id="55992-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="55992-124">En este ejemplo, se utiliza Glass en el área cliente para que parezca parte del marco.</span><span class="sxs-lookup"><span data-stu-id="55992-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="55992-125">Fotogramas ocultos</span><span class="sxs-lookup"><span data-stu-id="55992-125">Hidden frames</span></span>

<span data-ttu-id="55992-126">A veces, el marco de ventana mejor no es ningún fotograma.</span><span class="sxs-lookup"><span data-stu-id="55992-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="55992-127">Este suele ser el caso de la [ventana principal](glossary.md) de aplicaciones de [pantalla completa](glossary.md) que no se usan junto con otros programas, como reproductores multimedia, juegos y aplicaciones de quiosco.</span><span class="sxs-lookup"><span data-stu-id="55992-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="55992-128">Los visores de contenido a menudo se benefician de tener la opción de mostrar el contenido en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="55992-129">Algunos ejemplos son Windows Internet Explorer, Galería fotográfica de Windows Live, Windows Movie Maker HD, Microsoft PowerPoint y Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="55992-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="55992-130">captura de pantalla del reproductor de media en la vista de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="55992-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="55992-131">En este ejemplo, Windows Media Player puede mostrar su contenido en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="55992-132">Marcos personalizados</span><span class="sxs-lookup"><span data-stu-id="55992-132">Custom frames</span></span>

<span data-ttu-id="55992-133">La mayoría de las aplicaciones Windows deben usar los marcos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="55992-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="55992-134">Sin embargo, en el caso de las aplicaciones independientes, de pantalla completa e independiente, como los juegos y las aplicaciones de quiosco, puede ser adecuado utilizar fotogramas personalizados para las ventanas que no se muestran en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="55992-135">La motivación para usar fotogramas personalizados debe ser dar a la experiencia global una sensación única, no solo para la [Personalización de marca](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="55992-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="55992-136">Ilustración del rompecabezas y el fotograma de la imagen codificada</span><span class="sxs-lookup"><span data-stu-id="55992-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="55992-137">Los fotogramas personalizados son adecuados para aplicaciones independientes, de pantalla completa e independiente, como los juegos.</span><span class="sxs-lookup"><span data-stu-id="55992-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="55992-138">Directrices</span><span class="sxs-lookup"><span data-stu-id="55992-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="55992-139">Marcos de ventana</span><span class="sxs-lookup"><span data-stu-id="55992-139">Window frames</span></span>

-   <span data-ttu-id="55992-140">Usar marcos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="55992-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="55992-141">**Excepción:** Para proporcionar a las aplicaciones independientes una pantalla completa, una única sensación:</span><span class="sxs-lookup"><span data-stu-id="55992-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="55992-142">Considere la posibilidad de ocultar el marco de ventana de la [ventana principal](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="55992-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="55992-143">Considere la posibilidad de usar marcos personalizados para la [ventana secundaria](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="55992-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="55992-144">Si un fotograma personalizado es adecuado, elija un diseño ligero y no se Centre demasiado en ello.</span><span class="sxs-lookup"><span data-stu-id="55992-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="55992-145">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="55992-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="55992-146">captura de pantalla del marco distracción</span><span class="sxs-lookup"><span data-stu-id="55992-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="55992-147">En este ejemplo, el marco personalizado atrae demasiado atención a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="55992-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="55992-148">No agregue controles a un marco de ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="55992-149">Coloque los controles dentro de la ventana en su lugar.</span><span class="sxs-lookup"><span data-stu-id="55992-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="55992-150">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="55992-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="55992-151">captura de pantalla del control en el marco de ventana</span><span class="sxs-lookup"><span data-stu-id="55992-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="55992-152">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="55992-152">**Correct:**</span></span>

    ![<span data-ttu-id="55992-153">captura de pantalla del control en el área cliente</span><span class="sxs-lookup"><span data-stu-id="55992-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="55992-154">En el ejemplo correcto, el control está dentro del área cliente en lugar del marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="55992-155">Modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="55992-155">Full screen mode</span></span>

-   <span data-ttu-id="55992-156">Para los programas que tienen un modo de pantalla completa opcional, para habilitar el modo de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="55992-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="55992-157">Tener un comando de pantalla completa modal en la barra de menús o la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="55992-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="55992-158">Cuando el usuario haga clic en el comando, muestre el comando en su estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="55992-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="55992-159">captura de pantalla de la ventana con el elemento de menú de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="55992-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="55992-160">En este ejemplo se muestra el comando pantalla completa junto con su tecla de método abreviado estándar.</span><span class="sxs-lookup"><span data-stu-id="55992-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="55992-161">Utilice F11 para la tecla de método abreviado de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="55992-162">Si se usa normalmente una barra de herramientas y el modo de pantalla completa, también tiene un botón gráfico de la barra de herramientas con una información sobre herramientas de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="55992-163">captura de pantalla de los botones pantalla completa y revertir</span><span class="sxs-lookup"><span data-stu-id="55992-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="55992-164">Ejemplos de botones de la barra de herramientas de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="55992-165">Para volver al modo de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="55992-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="55992-166">Tener un comando de pantalla completa modal en la barra de menús o la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="55992-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="55992-167">Cuando el usuario haga clic en el comando, muestre el comando en su estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="55992-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="55992-168">Utilice F11 para la tecla de método abreviado de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="55992-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="55992-169">Si aún no se ha asignado, ESC también puede usarse para este fin.</span><span class="sxs-lookup"><span data-stu-id="55992-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="55992-170">Vidrio</span><span class="sxs-lookup"><span data-stu-id="55992-170">Glass</span></span>

<span data-ttu-id="55992-171">Los marcos de ventana estándar usan cristal automáticamente en Windows, pero también puede usar Glass en regiones que tocan el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="55992-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="55992-172">**Considere la posibilidad de usar Glass estratégicamente en regiones pequeñas que tocan el marco de la ventana sin texto.**</span><span class="sxs-lookup"><span data-stu-id="55992-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="55992-173">Si lo hace, puede dar un aspecto más sencillo, más ligero y coherente haciendo que la región parezca parte del marco.</span><span class="sxs-lookup"><span data-stu-id="55992-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="55992-174">captura de pantalla de la ventana con borde translúcido</span><span class="sxs-lookup"><span data-stu-id="55992-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="55992-175">En este ejemplo, cristal centra la atención del usuario sobre el contenido en lugar de los controles.</span><span class="sxs-lookup"><span data-stu-id="55992-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="55992-176">**No use cristal en situaciones en las que un fondo de ventana sin formato sea más atractivo o fácil de usar.**</span><span class="sxs-lookup"><span data-stu-id="55992-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="55992-177">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="55992-177">**Correct:**</span></span>

![<span data-ttu-id="55992-178">captura de pantalla de la ventana con cuatro gráficos y etiquetas</span><span class="sxs-lookup"><span data-stu-id="55992-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="55992-179">En este ejemplo, Glass se usa para dar una apariencia ligera a la ventana Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="55992-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="55992-180">Glass funciona para esta ventana porque consta de gráficos y una sola etiqueta de texto segura.</span><span class="sxs-lookup"><span data-stu-id="55992-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="55992-181">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="55992-181">**Incorrect:**</span></span>

![<span data-ttu-id="55992-182">captura de pantalla de la ventana con doce gráficos</span><span class="sxs-lookup"><span data-stu-id="55992-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="55992-183">En este ejemplo incorrecto, el uso de cristal es distracción.</span><span class="sxs-lookup"><span data-stu-id="55992-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="55992-184">Un fondo de ventana simple sería una opción mejor.</span><span class="sxs-lookup"><span data-stu-id="55992-184">A plain window background would be a better choice.</span></span>

 

 