---
description: Cuando esté listo para depurar la funcionalidad de COM+ en los componentes de Microsoft Visual C++, puede configurar Visual C++ proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Depurar componentes escritos en Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705270"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="83421-103">Depurar componentes escritos en Visual C++</span><span class="sxs-lookup"><span data-stu-id="83421-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="83421-104">Cuando esté listo para depurar la funcionalidad de COM+ en los componentes de Microsoft Visual C++, puede configurar Visual C++ proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="83421-105">Si usa Visual C++, puede depurar con un cliente remoto mediante la depuración Just-in-Time (JIT) y OLE RPC.</span><span class="sxs-lookup"><span data-stu-id="83421-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="83421-106">Si no puede ejecutar el cliente en el depurador o si el cliente se está ejecutando en otro equipo, puede usar la configuración **Inicio de com+ en el depurador** .</span><span class="sxs-lookup"><span data-stu-id="83421-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="83421-107">Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla en la pestaña **Opciones avanzadas** del cuadro de diálogo **propiedades** de la aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="83421-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="83421-108">Cuando haya terminado la depuración, debe cerrar las aplicaciones COM+ que está depurando.</span><span class="sxs-lookup"><span data-stu-id="83421-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="83421-109">Si se deja de ejecutar un proceso de servidor, es posible que reciba un mensaje de error la próxima vez que intente compilar un archivo DLL cuando el archivo DLL existente todavía esté cargado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="83421-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="83421-110">Para cerrar una aplicación COM+, haga clic con el botón secundario en la aplicación en el árbol de consola y, a continuación, haga clic en **apagar**.</span><span class="sxs-lookup"><span data-stu-id="83421-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="83421-111">Si utiliza transacciones, es posible que también desee aumentar el tiempo de espera de la transacción, cuyo valor predeterminado es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="83421-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="83421-112">También puede especificar un valor de 0, con lo que se especifica de forma eficaz un período de tiempo de espera de transacción infinito.</span><span class="sxs-lookup"><span data-stu-id="83421-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="83421-113">Use la herramienta administrativa Servicios de componentes para cambiar el valor de tiempo de espera de la transacción en la pestaña **Opciones** de la ventana **propiedades de mi PC** .</span><span class="sxs-lookup"><span data-stu-id="83421-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="83421-114">Depurar componentes de la aplicación de servidor con Visual C++</span><span class="sxs-lookup"><span data-stu-id="83421-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="83421-115">Al depurar las aplicaciones de servidor COM+, es posible que desee depurar las llamadas remotas cargando tanto el cliente como la aplicación de servidor en el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="83421-116">Con Visual C++, puede depurar las llamadas remotas a los componentes a través de la configuración Just-in-Time (JIT) y OLE RPC.</span><span class="sxs-lookup"><span data-stu-id="83421-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="83421-117">La configuración JIT hace que el componente compilado inicie el depurador de Visual C++ cuando se produce un error. la configuración de OLE RPC permite al depurador pasar del cliente al componente mientras se recorre el código.</span><span class="sxs-lookup"><span data-stu-id="83421-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="83421-118">Cuando estas características están habilitadas, puede iniciar el cliente en el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="83421-119">Cuando el cliente realiza una llamada al componente, el depurador entrará en el código del componente en el proceso del servidor, incluso si el servidor está en un equipo diferente de la red.</span><span class="sxs-lookup"><span data-stu-id="83421-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="83421-120">Si es necesario, se inicia automáticamente una sesión de depuración en el equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="83421-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="83421-121">Del mismo modo, la ejecución paso a paso después de la instrucción return en el código del componente devolverá la depuración a la siguiente instrucción en el código del cliente.</span><span class="sxs-lookup"><span data-stu-id="83421-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="83421-122">Es posible que pueda guardar algunos pasos mediante el uso de la configuración **de inicio de com+ en el depurador** .</span><span class="sxs-lookup"><span data-stu-id="83421-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="83421-123">Esto le permite especificar el depurador Visual C++ (u otro) sin tener que realizar una configuración de depuración especial en el entorno de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="83421-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="83421-124">Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla en la pestaña **Opciones avanzadas** del cuadro de diálogo **propiedades** de la aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="83421-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="83421-125">Para obtener más información, vea "depuración sin Visual C++" en este tema.</span><span class="sxs-lookup"><span data-stu-id="83421-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="83421-126">Cuando la aplicación COM+ que contiene el componente es una aplicación de servidor, debe empezar por cerrar la aplicación mediante la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="83421-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="83421-127">Para ello, haga clic con el botón secundario en la aplicación COM+ en el árbol de consola y, a continuación, haga clic en **apagar**.</span><span class="sxs-lookup"><span data-stu-id="83421-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="83421-128">**Para habilitar la depuración RPC en Visual C++**</span><span class="sxs-lookup"><span data-stu-id="83421-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="83421-129">En Visual C++, en el menú **herramientas** , haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="83421-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="83421-130">En el cuadro de diálogo **Opciones** , en la pestaña **depurar** , active las casillas depuración de **OLE RPC** y **depuración Just-in-Time** .</span><span class="sxs-lookup"><span data-stu-id="83421-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="83421-131">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="83421-131">Click **OK**.</span></span>

<span data-ttu-id="83421-132">Para comenzar la depuración, inicie el proyecto de cliente en el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="83421-133">También puede depurar el componente sin iniciar el cliente en el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="83421-134">En este caso, el componente debe iniciar el depurador por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="83421-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="83421-135">Para ello, el proyecto de componente debe especificar un archivo ejecutable para la sesión de depuración, junto con el identificador de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="83421-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="83421-136">**Para permitir que un componente de aplicación de servidor inicie el depurador de Visual C++**</span><span class="sxs-lookup"><span data-stu-id="83421-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="83421-137">En el menú **proyecto** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="83421-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="83421-138">En el cuadro de diálogo **configuración del proyecto** , en el cuadro **configuración para** , seleccione **depuración de Win32**.</span><span class="sxs-lookup"><span data-stu-id="83421-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="83421-139">En la pestaña **depurar** , en el cuadro **categoría** , seleccione **General**.</span><span class="sxs-lookup"><span data-stu-id="83421-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="83421-140">En el cuadro **ejecutable para sesión de depuración** , escriba la ruta de acceso completa de Dllhost.exe, seguido de un argumento que especifique el identificador de la aplicación com+ que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="83421-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="83421-141">Con la herramienta administrativa Servicios de componentes, encontrará el identificador de la aplicación en la pestaña **General** del cuadro de diálogo **propiedades** de la aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="83421-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="83421-142">El siguiente es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="83421-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="83421-143">C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: {applicationID}</span><span class="sxs-lookup"><span data-stu-id="83421-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="83421-144">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="83421-144">Click **OK**.</span></span>

<span data-ttu-id="83421-145">Ahora puede establecer puntos de interrupción, iniciar el depurador y comenzar a realizar llamadas al componente.</span><span class="sxs-lookup"><span data-stu-id="83421-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="83421-146">Depurar componentes de aplicación de biblioteca con Visual C++</span><span class="sxs-lookup"><span data-stu-id="83421-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="83421-147">Para depurar componentes en una aplicación de biblioteca, debe configurar el proyecto del cliente porque el proceso del cliente hospedará la aplicación de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="83421-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="83421-148">**Para habilitar la depuración de aplicaciones de biblioteca con Visual C++**</span><span class="sxs-lookup"><span data-stu-id="83421-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="83421-149">En Visual C++, en el menú **proyecto** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="83421-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="83421-150">En el cuadro de diálogo **configuración del proyecto** , en el cuadro **configuración de** , haga clic en **depuración de Win32**.</span><span class="sxs-lookup"><span data-stu-id="83421-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="83421-151">En la pestaña **depurar** , en el cuadro **categoría** , haga clic en **archivos dll adicionales**.</span><span class="sxs-lookup"><span data-stu-id="83421-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="83421-152">En la lista **módulos** , agregue los archivos DLL del componente en la aplicación de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="83421-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="83421-153">Esto le permite establecer puntos de interrupción antes de que se cargue realmente el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="83421-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="83421-154">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="83421-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="83421-155">Depuración sin Visual C++</span><span class="sxs-lookup"><span data-stu-id="83421-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="83421-156">Tanto si usa como si no Visual C++ para la depuración, puede usar la configuración **iniciar en el depurador** para especificar el depurador en el que deben ejecutarse los componentes.</span><span class="sxs-lookup"><span data-stu-id="83421-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="83421-157">**Para especificar un depurador desde la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="83421-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="83421-158">En el árbol de consola, seleccione la aplicación de biblioteca COM+ que contiene los componentes que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="83421-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="83421-159">Haga clic con el botón secundario en la aplicación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="83421-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="83421-160">En el cuadro de diálogo **propiedades** de la aplicación, haga clic en la pestaña **Opciones avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="83421-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="83421-161">En **depuración**, active la casilla **iniciar en el depurador** .</span><span class="sxs-lookup"><span data-stu-id="83421-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="83421-162">En el cuadro **ruta de acceso del depurador** , escriba la ruta de acceso al depurador que desee usar.</span><span class="sxs-lookup"><span data-stu-id="83421-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="83421-163">También puede hacer clic en **examinar** para buscar el depurador.</span><span class="sxs-lookup"><span data-stu-id="83421-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="83421-164">A continuación se encuentra un ejemplo: C: \\ WinNT \\ system32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="83421-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="83421-165">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="83421-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83421-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83421-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83421-167">Depurar componentes escritos en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="83421-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



