---
title: Usar máscaras con el control Media Player de Windows
description: Usar máscaras con el control Media Player de Windows
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
- Control ActiveX de Windows Media Player, máscaras
- Control ActiveX móvil de Windows Media Player, máscaras
- Control ActiveX, máscaras
- máscaras, incrustar el control ActiveX
- Aspectos de Windows Media Player, incrustar el control ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268812"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="f2d2e-124">Usar máscaras con el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="f2d2e-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="f2d2e-125">Al incrustar el control Media Player de Windows en un programa de C++, puede personalizar la interfaz de usuario (UI) del reproductor aplicando un archivo de definición de máscara a él.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="f2d2e-126">Un archivo de definición de máscara es un documento basado en XML que especifica el diseño de componentes de interfaz de usuario estándar y personalizables y los gráficos que lo acompañan.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="f2d2e-127">Con Microsoft JScript, puede especificar el comportamiento de estos componentes y manipular el control de Media Player de Windows sin la sobrecarga de C++ y la sintaxis COM.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="f2d2e-128">Las máscaras proporcionan una manera fácil de mantener el código de la interfaz de usuario y el código de programa principal por separado para que se puedan mantener y desarrollar de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="f2d2e-129">También puede reutilizar máscaras diseñadas originalmente para su uso por parte del reproductor independiente en modo de máscara.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="f2d2e-130">El código de máscara diseñado específicamente para los programas de C++ puede interactuar con los programas a través de un objeto que puede incluirse en scripts y que el programa puede proporcionar.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="f2d2e-131">Para habilitar el modo de máscara para el control Media Player de Windows, el programa debe implementar la interfaz **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="f2d2e-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="f2d2e-132">Aunque puede usar máscaras con el control y el control remoto al mismo tiempo, puede usar esta interfaz para habilitar cualquiera de las características sin habilitar la otra.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="f2d2e-133">Para deshabilitar la comunicación remota, solo tiene que pasar un valor "local" como parámetro out del método **GetServiceType** y devolver un valor HRESULT de E \_ NOTIMPL desde el método **GetApplicationName** .</span><span class="sxs-lookup"><span data-stu-id="f2d2e-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="f2d2e-134">Para cambiar el control de Media Player de Windows al modo de máscara, llame al método **IWMPPlayer::p UT \_ uiMode** , pasando un valor de "Custom".</span><span class="sxs-lookup"><span data-stu-id="f2d2e-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="f2d2e-135">Especifique la ruta de acceso y el nombre de archivo del archivo de definición de máscara que se va a usar devolviéndolo desde el método **IWMPRemoteMediaServices:: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="f2d2e-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="f2d2e-136">Si desea proporcionar un objeto que admite scripts para la comunicación entre la máscara y el programa, pase un nombre y un puntero a un puntero **IDispatch** como los dos parámetros out del método **IWMPRemoteMediaServices:: GetScriptableObject** .</span><span class="sxs-lookup"><span data-stu-id="f2d2e-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="f2d2e-137">Después, la máscara puede realizar llamadas al objeto que admite scripts mediante el uso del nombre especificado como si fuera un atributo global similar al atributo global del **reproductor** .</span><span class="sxs-lookup"><span data-stu-id="f2d2e-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="f2d2e-138">Una máscara aplicada a un control de Windows Media Player remoto puede tener acceso al objeto **PlayerApplication** mediante otro atributo global denominado **PlayerApplication**.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="f2d2e-139">Dado que las máscaras no pueden tener acceso a la propiedad **Player. playerApplication** , debe usar este atributo global cuando desee que el código de máscara administre el acoplamiento y desacoplamiento.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="f2d2e-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f2d2e-140">Samples</span></span>

<span data-ttu-id="f2d2e-141">El paquete de instalación de Windows Media Player SDK instala un ejemplo que muestra cómo aplicar una máscara al control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="f2d2e-142">Vea el ejemplo RemoteSkin para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2d2e-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2d2e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d2e-144">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="f2d2e-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="f2d2e-145">**Usar el control Media Player de Windows en un programa de C++**</span><span class="sxs-lookup"><span data-stu-id="f2d2e-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




