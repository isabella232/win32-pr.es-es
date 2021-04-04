---
title: Usar el control Media Player de Windows con Microsoft Visual Studio
description: Usar el control Media Player de Windows con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, .NET Framework
- Modelo de objetos de Windows Media Player, .NET Framework
- modelo de objetos, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Control ActiveX de Windows Media Player, .NET Framework
- Control ActiveX móvil de Windows Media Player, .NET Framework
- Control ActiveX, .NET Framework
- Control ActiveX de Windows Media Player, Visual Studio
- Control ActiveX móvil de Windows Media Player, Visual Studio
- Control ActiveX, Visual Studio
- .NET Framework, inserción de programas de Visual Studio
- incrustación, programas de Visual Studio
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104076425"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="0437f-123">Usar el control Media Player de Windows con Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0437f-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="0437f-124">Puede Agregar la serie Windows Media Player 9 o el control ActiveX posterior a una aplicación .NET Framework a través del cuadro de herramientas de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0437f-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="0437f-125">Agregar el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="0437f-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="0437f-126">Antes de crear un nuevo proyecto, asegúrese de que la versión más reciente de Windows Media Player y el SDK de Windows Media Player está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="0437f-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="0437f-127">Inicie Visual Studio y, a continuación, cree un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="0437f-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="0437f-128">En Visual Studio, abra el cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="0437f-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="0437f-129">Si Windows Media Player no aparece en la parte **componentes** del cuadro de herramientas, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0437f-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="0437f-130">Haga clic con el botón derecho en el cuadro de herramientas y seleccione **elegir elementos**.</span><span class="sxs-lookup"><span data-stu-id="0437f-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="0437f-131">Se abrirá el cuadro de diálogo Personalizar cuadro de **herramientas** .</span><span class="sxs-lookup"><span data-stu-id="0437f-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="0437f-132">En la pestaña **componentes com** , seleccione Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0437f-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="0437f-133">Si Windows Media Player no aparece en la lista, haga clic en **examinar** y, a continuación, abra Wmp.dll, que debe estar en la \\ carpeta system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="0437f-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="0437f-134">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="0437f-134">Click **OK**.</span></span> <span data-ttu-id="0437f-135">El control Media Player de Windows se colocará en la pestaña actual del cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="0437f-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="0437f-136">Ahora puede seleccionar Windows Media Player en el cuadro de herramientas y agregarlo a un formulario.</span><span class="sxs-lookup"><span data-stu-id="0437f-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="0437f-137">Visual Studio proporciona a Windows Media Player control un nombre predeterminado como "axWindowsMediaPlayer1".</span><span class="sxs-lookup"><span data-stu-id="0437f-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="0437f-138">Puede que desee cambiar el nombre por algo más fácil de recordar, como "reproductor".</span><span class="sxs-lookup"><span data-stu-id="0437f-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="0437f-139">Al agregar el control Media Player de Windows desde el cuadro de herramientas, también se agregan referencias a dos bibliotecas creadas por Visual Studio, AxWMPLib y WMPLib.</span><span class="sxs-lookup"><span data-stu-id="0437f-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="0437f-140">Puede encontrarlos en el Explorador de soluciones en **referencias**.</span><span class="sxs-lookup"><span data-stu-id="0437f-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="0437f-141">Para facilitar el uso de los objetos del espacio de nombres del reproductor, debe incluir el espacio de nombres en las directivas Using o Imports de los archivos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="0437f-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="0437f-142">La Directiva garantiza que puede hacer referencia a los objetos de **reproductor** sin calificar completamente sus nombres.</span><span class="sxs-lookup"><span data-stu-id="0437f-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="0437f-143">El control Media Player de Windows es un objeto **AxWindowsMediaPlayer** del espacio de nombres **AxWMPLib** .</span><span class="sxs-lookup"><span data-stu-id="0437f-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="0437f-144">Sin embargo, la clase **AxWindowsMediaPlayer** usa tipos de datos, interfaces y otros elementos del espacio de nombres **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="0437f-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="0437f-145">Configurar la visibilidad del control</span><span class="sxs-lookup"><span data-stu-id="0437f-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="0437f-146">Cuando agregue por primera vez el control de Media Player de Windows a un formulario, será visible.</span><span class="sxs-lookup"><span data-stu-id="0437f-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="0437f-147">Si no desea usar la imagen visible del reproductor en la aplicación, oculte el reproductor predeterminado estableciendo cualquiera de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="0437f-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="0437f-148">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0437f-148">Property</span></span>        | <span data-ttu-id="0437f-149">Value</span><span class="sxs-lookup"><span data-stu-id="0437f-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="0437f-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="0437f-150">**uiMode**</span></span>      | <span data-ttu-id="0437f-151">"invisible" (vea [Player. uiMode](player-uimode.md)).</span><span class="sxs-lookup"><span data-stu-id="0437f-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="0437f-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="0437f-152">**Visible**</span></span>     | <span data-ttu-id="0437f-153">"false"</span><span class="sxs-lookup"><span data-stu-id="0437f-153">"false"</span></span>                                               |
| <span data-ttu-id="0437f-154">**Tamaño. ancho**</span><span class="sxs-lookup"><span data-stu-id="0437f-154">**Size.Width**</span></span>  | <span data-ttu-id="0437f-155">0</span><span class="sxs-lookup"><span data-stu-id="0437f-155">0</span></span>                                                     |
| <span data-ttu-id="0437f-156">**Tamaño. alto**</span><span class="sxs-lookup"><span data-stu-id="0437f-156">**Size.Height**</span></span> | <span data-ttu-id="0437f-157">0</span><span class="sxs-lookup"><span data-stu-id="0437f-157">0</span></span>                                                     |



 

<span data-ttu-id="0437f-158">Puede establecer estas propiedades en el código o en la ventana **propiedades** cuando se selecciona el control Media Player de Windows en el diseñador de formularios.</span><span class="sxs-lookup"><span data-stu-id="0437f-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="0437f-159">Compatibilidad del modelo de objetos del control</span><span class="sxs-lookup"><span data-stu-id="0437f-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="0437f-160">El modelo de objetos para el control Media Player de Windows es básicamente el mismo en el .NET Framework como en el script y el código no administrado.</span><span class="sxs-lookup"><span data-stu-id="0437f-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="0437f-161">Sin embargo, hay diferencias en el modo en que se exponen los elementos:</span><span class="sxs-lookup"><span data-stu-id="0437f-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="0437f-162">La mayoría de los objetos se exponen bajo el nombre de la interfaz COM subyacente.</span><span class="sxs-lookup"><span data-stu-id="0437f-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="0437f-163">Por ejemplo, el objeto de **lista de reproducción** se expone como **IWMPPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="0437f-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="0437f-164">Algunas interfaces tienen versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0437f-164">Some interfaces have later versions.</span></span> <span data-ttu-id="0437f-165">Por ejemplo, a **IWMPMedia** se le proporcionó funcionalidad adicional en **IWMPMedia2** y **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="0437f-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="0437f-166">Si declara un objeto como **IWMPMedia**, normalmente tiene acceso a la funcionalidad de todas las versiones de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0437f-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="0437f-167">Sin embargo, IntelliSense® no reconocerá los métodos o las propiedades de las interfaces de versiones posteriores, y el editor de .NET de Visual Basic no corregirá automáticamente las mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="0437f-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="0437f-168">Para obtener todas las ventajas de IntelliSense y otras características de Visual Studio, declare el objeto con la versión más reciente de la interfaz, como **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="0437f-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="0437f-169">No hay propiedades indizadas (C#) o propiedades predeterminadas (Visual Basic .NET).</span><span class="sxs-lookup"><span data-stu-id="0437f-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="0437f-170">Por ejemplo, para recuperar un **elemento playlist. Item**, debe llamar al método de descriptor de acceso **IWMPlaylist. Get \_ Item** en C# o recuperar la propiedad **IWMPlayist. Item** en Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="0437f-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="0437f-171">Debido a un conflicto de nombres entre la propiedad de los **controles** de Windows Media Player y la propiedad **Controls** expuesta por cada control, la versión del reproductor de esta propiedad se denomina **CtlControls** en el contexto del control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="0437f-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="0437f-172">(Sin embargo, esto no es así cuando se crea el reproductor mediante programación, en lugar de como un control ActiveX).</span><span class="sxs-lookup"><span data-stu-id="0437f-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="0437f-173">Use el Examinador de objetos de Visual Studio para buscar los nombres de API correctos para los métodos y objetos de los espacios de nombres **AxWMPLib** y **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="0437f-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="0437f-174">Distribuir la aplicación</span><span class="sxs-lookup"><span data-stu-id="0437f-174">Distributing Your Application</span></span>

<span data-ttu-id="0437f-175">Al distribuir la aplicación, asegúrese de instalar AxInterop.WMPLib.dll y Interop.WMPLib.dll en la carpeta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0437f-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="0437f-176">También debe asegurarse de que la versión de Windows Media Player requerida esté instalada en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0437f-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0437f-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0437f-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0437f-178">**Crear el control Media Player de Windows mediante programación**</span><span class="sxs-lookup"><span data-stu-id="0437f-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="0437f-179">**Incrustar el control Media Player de Windows en una solución de C#**</span><span class="sxs-lookup"><span data-stu-id="0437f-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="0437f-180">**Incrustar el control Media Player de Windows en una solución Visual Basic .NET**</span><span class="sxs-lookup"><span data-stu-id="0437f-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




