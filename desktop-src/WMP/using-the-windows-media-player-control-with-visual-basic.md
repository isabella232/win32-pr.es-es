---
title: Usar el control Media Player de Windows con Visual Basic
description: Usar el control Media Player de Windows con Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Media Player de Windows, Visual Basic
- Modelo de objetos de Windows Media Player, Visual Basic
- modelo de objetos, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Control ActiveX de Windows Media Player, Visual Basic
- Control ActiveX de Windows Media Player Mobile, Visual Basic
- Control ActiveX, Visual Basic
- Incrustación de programas basados en Visual Basic
- incrustación, programas basados en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357312"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="728ba-119">Usar el control Media Player de Windows con Visual Basic</span><span class="sxs-lookup"><span data-stu-id="728ba-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="728ba-120">En esta sección se describe cómo usar la serie Windows Media Player 9 o el control ActiveX posterior en aplicaciones creadas con Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="728ba-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="728ba-121">Introducción</span><span class="sxs-lookup"><span data-stu-id="728ba-121">Getting Started</span></span>

<span data-ttu-id="728ba-122">Para agregar el control Media Player de Windows al cuadro de herramientas, primero seleccione **componentes** en el menú **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="728ba-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="728ba-123">En el cuadro de diálogo componentes, active la casilla situada junto a "Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="728ba-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="728ba-124">En la parte inferior del cuadro de diálogo, confirme que el archivo seleccionado está wmp.dll.</span><span class="sxs-lookup"><span data-stu-id="728ba-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="728ba-125">Después de cerrar el cuadro de diálogo, puede colocar una instancia del control Media Player de Windows en el formulario de la manera habitual.</span><span class="sxs-lookup"><span data-stu-id="728ba-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="728ba-126">Puede establecer muchas propiedades de control mediante el ventana Propiedades.</span><span class="sxs-lookup"><span data-stu-id="728ba-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="728ba-127">Para establecer algunas propiedades, debe usar el cuadro de diálogo Propiedades de Media Player de Windows, que se abre con el elemento "(personalizado)" en el ventana Propiedades.</span><span class="sxs-lookup"><span data-stu-id="728ba-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="728ba-128">Referencias a objetos</span><span class="sxs-lookup"><span data-stu-id="728ba-128">Object References</span></span>

<span data-ttu-id="728ba-129">Puede usar ciertas propiedades de control del reproductor para obtener referencias a objetos concretos.</span><span class="sxs-lookup"><span data-stu-id="728ba-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="728ba-130">Por ejemplo, la propiedad **cdromCollection** devuelve una referencia a un objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="728ba-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="728ba-131">Debe asignar este tipo de referencia a una variable que declaró como la interfaz correspondiente.</span><span class="sxs-lookup"><span data-stu-id="728ba-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="728ba-132">Por ejemplo, en el caso de la propiedad **cdromCollection** , se asigna el valor devuelto a una variable de tipo **IWMPCdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="728ba-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="728ba-133">Lea el tema [interfaces](interfaces.md) en la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md) para identificar qué objetos implementan varias interfaces.</span><span class="sxs-lookup"><span data-stu-id="728ba-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="728ba-134">En esos casos, debe declarar una variable de objeto como la interfaz con el número más alto documentada en este SDK para tener acceso a todas las propiedades y los métodos de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="728ba-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="728ba-135">Por ejemplo, debe asignar el valor de la propiedad **currentMedia** de control de Windows Media Player a una variable declarada como **IWMPMedia3** para asegurarse de que tiene acceso a los métodos **getAttributeCountByType** y **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="728ba-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="728ba-136">El objeto **WindowsMediaPlayer** implementa todas las propiedades y los métodos de las interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** y **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="728ba-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="728ba-137">No es necesario declarar variables independientes para cualquiera de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="728ba-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="728ba-138">Puede tener acceso a todos sus miembros mediante el nombre que asignó a la instancia de **WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="728ba-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="728ba-139">En el Visual Basic Examinador de objetos verá muchas interfaces que están destinadas al uso privado del control de Media Player de Windows, incluidos algunos que admiten desarrolladores de máscaras.</span><span class="sxs-lookup"><span data-stu-id="728ba-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="728ba-140">Solo debe usar los objetos, las propiedades, los métodos y los eventos que se documentan en este SDK.</span><span class="sxs-lookup"><span data-stu-id="728ba-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="728ba-141">Consejos adicionales</span><span class="sxs-lookup"><span data-stu-id="728ba-141">Additional Tips</span></span>

-   <span data-ttu-id="728ba-142">La documentación de referencia muestra la sintaxis de JScript.</span><span class="sxs-lookup"><span data-stu-id="728ba-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="728ba-143">En JScript, los argumentos pasados a los métodos siempre se incluyen entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="728ba-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="728ba-144">En Visual Basic 6,0, los argumentos pasados a métodos que no devuelven un valor no se deben incluir entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="728ba-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="728ba-145">Es posible que algunas propiedades o métodos no aparezcan en la característica lista automática de finalización de código en el editor de código de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="728ba-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="728ba-146">Puede seguir usando estos miembros escribiendo sus nombres exactamente como aparecen en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="728ba-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="728ba-147">Administrar la apariencia visual del control mediante la propiedad **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="728ba-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="728ba-148">Puede hacerlo de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="728ba-148">You can do so in two ways.</span></span> <span data-ttu-id="728ba-149">Puede usar la lista desplegable **seleccionar un modo** del cuadro de diálogo Propiedades de Windows Media Player, o bien puede escribir el valor correcto en el ventana Propiedades.</span><span class="sxs-lookup"><span data-stu-id="728ba-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="728ba-150">En concreto, no utilice la propiedad **visible** para ocultar el control; en su lugar, asigne el valor "invisible" a la propiedad **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="728ba-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="728ba-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="728ba-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="728ba-152">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="728ba-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




