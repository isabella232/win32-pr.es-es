---
title: Crear una aplicación de cinta
description: El marco de la cinta de Windows se compone de dos plataformas de desarrollo distintas, pero dependientes, un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basado en el modelo de objetos componentes (COM) de C++ para definir la funcionalidad de comandos y los enlaces de la aplicación. Esta división de mano de obra dentro de la arquitectura del marco de cinta requiere que un desarrollador que desee aprovechar las capacidades enriquecidas de la interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de cinta para conectar el marco de trabajo a la aplicación host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Cinta de Windows, crear aplicaciones
- Cinta, crear aplicaciones
- Cinta de opciones de Windows, mapa de ruta
- Cinta, guía básica
- Cinta de Windows, marcado
- Cinta de opciones, marcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421137"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="5e509-110">Crear una aplicación de cinta</span><span class="sxs-lookup"><span data-stu-id="5e509-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="5e509-111">El marco de la cinta de opciones de Windows se compone de dos plataformas de desarrollo distintas pero dependientes: un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basado en el modelo de objetos componentes (COM) de C++ para definir la funcionalidad del comando y los enlaces de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="5e509-112">Esta división de mano de obra dentro de la arquitectura del marco de cinta requiere que un desarrollador que desee aprovechar las capacidades enriquecidas de la interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de cinta para conectar el marco de trabajo a la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="5e509-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="5e509-113">Guía básica de la cinta</span><span class="sxs-lookup"><span data-stu-id="5e509-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="5e509-114">Escribir el marcado</span><span class="sxs-lookup"><span data-stu-id="5e509-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="5e509-115">Compilar el marcado</span><span class="sxs-lookup"><span data-stu-id="5e509-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="5e509-116">Compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="5e509-117">Inicializar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="5e509-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="5e509-118">Vincular el marcado a la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="5e509-119">Compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="5e509-120">Actualizaciones y ejecuciones en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5e509-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="5e509-121">Compatibilidad con OLE</span><span class="sxs-lookup"><span data-stu-id="5e509-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="5e509-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e509-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="5e509-123">Guía básica de la cinta</span><span class="sxs-lookup"><span data-stu-id="5e509-123">Ribbon Roadmap</span></span>

<span data-ttu-id="5e509-124">Los aspectos visuales de una aplicación de la cinta de opciones, como los controles que se muestran y dónde se colocan, se declaran en el marcado (vea [declarar comandos y controles con el marcado de la cinta de](windowsribbon-schema.md)opciones).</span><span class="sxs-lookup"><span data-stu-id="5e509-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="5e509-125">La lógica de comandos de la aplicación, como lo que sucede cuando se presiona un botón, se implementa en el código.</span><span class="sxs-lookup"><span data-stu-id="5e509-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="5e509-126">El proceso de implementación de una cinta de opciones y su incorporación en una aplicación Windows requiere cuatro tareas básicas: escribir el marcado, compilar el marcado, escribir el código y compilar y vincular toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="5e509-127">En el diagrama siguiente se ilustra el flujo de trabajo para una implementación de cinta de opciones típica.</span><span class="sxs-lookup"><span data-stu-id="5e509-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![diagrama que muestra el flujo de trabajo para una implementación de cinta típica.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="5e509-129">En las secciones siguientes se describe este proceso con más detalle.</span><span class="sxs-lookup"><span data-stu-id="5e509-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="5e509-130">Escribir el marcado</span><span class="sxs-lookup"><span data-stu-id="5e509-130">Write the Markup</span></span>

<span data-ttu-id="5e509-131">Una vez diseñada la interfaz de usuario de la cinta de opciones, la primera tarea para el desarrollador de la aplicación es describir la interfaz de usuario con el marcado de la cinta.</span><span class="sxs-lookup"><span data-stu-id="5e509-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e509-132">El archivo de esquema de marcado del marco de cinta, UICC. xsd, se instala con el kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0.</span><span class="sxs-lookup"><span data-stu-id="5e509-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="5e509-133">Con la ruta de instalación estándar, el archivo se encuentra en la carpeta% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ número \] \\ bin, donde se puede hacer referencia a él mediante muchos editores XML para proporcionar sugerencias y la finalización automática.</span><span class="sxs-lookup"><span data-stu-id="5e509-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="5e509-134">Controles de la cinta de opciones, comandos de la cinta de opciones (los elementos independientes del control que proporcionan la funcionalidad básica para los controles de la cinta) y todas las relaciones visuales y de diseño del control se declaran en el marcado.</span><span class="sxs-lookup"><span data-stu-id="5e509-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="5e509-135">La estructura del marcado de la cinta de opciones destaca la distinción entre los controles y comandos de la cinta de opciones a través de dos jerarquías de nodos principales: un árbol de [comandos y recursos](windowsribbon-reference-elements-command.md) y un árbol de [vistas](windowsribbon-reference-elements-view.md) .</span><span class="sxs-lookup"><span data-stu-id="5e509-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="5e509-136">Todos los contenedores y las acciones que expone la cinta de opciones se declaran en el árbol de [comandos y recursos](windowsribbon-reference-elements-command.md) .</span><span class="sxs-lookup"><span data-stu-id="5e509-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="5e509-137">Cada elemento de comando está asociado a un conjunto de recursos, tal y como requiere el diseño de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e509-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="5e509-138">Después de crear los comandos para una aplicación, se declaran los controles en el árbol de [vistas](windowsribbon-reference-elements-view.md) y se enlaza cada control a un comando para exponer la funcionalidad del comando.</span><span class="sxs-lookup"><span data-stu-id="5e509-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="5e509-139">El marco de cinta determina el posicionamiento real de los controles en función de la jerarquía de controles declarada aquí.</span><span class="sxs-lookup"><span data-stu-id="5e509-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="5e509-140">En el ejemplo de código siguiente se muestra cómo declarar un control de botón, con la etiqueta aplicación de salida, y asociarlo a un comando de salida.</span><span class="sxs-lookup"><span data-stu-id="5e509-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="5e509-141">Aunque es posible usar cualquier extensión de nombre de archivo para el archivo de marcado de la cinta,. XML es la extensión recomendada que se utiliza en toda la documentación.</span><span class="sxs-lookup"><span data-stu-id="5e509-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="5e509-142">Compilar el marcado</span><span class="sxs-lookup"><span data-stu-id="5e509-142">Compile the Markup</span></span>

<span data-ttu-id="5e509-143">Una vez creado el archivo de marcado de la cinta de opciones, el compilador de marcado de la cinta de opciones (UICC), que se incluye con el kit de desarrollo de software (SDK) de Windows, debe compilarse en un formato binario.</span><span class="sxs-lookup"><span data-stu-id="5e509-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="5e509-144">Una referencia a este archivo binario se pasa al método [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante la inicialización del marco de la cinta de opciones de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="5e509-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="5e509-145">UICC se puede ejecutar directamente desde una ventana de línea de comandos o agregarse como un "paso de compilación personalizada" en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5e509-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="5e509-146">En la imagen siguiente se muestra el compilador de marcado UICC en la ventana de Shell CMD del SDK de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e509-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![captura de pantalla que muestra uicc.exe en una ventana de línea de comandos.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="5e509-148">La siguiente imagen muestra UICC agregado como un paso de compilación personalizado en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5e509-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![captura de pantalla que muestra uicc.exe agregado como un paso de compilación personalizado en Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="5e509-150">UICC genera tres archivos: una versión binaria del marcado (. BML), un encabezado de definición de identificador (archivo. h) para exponer los elementos de marcado en la aplicación host de la cinta de opciones y un [script de definición de recursos](../menurc/about-resource-files.md) (archivo. RC) para vincular los recursos de cadena y imagen de la cinta de opciones a la aplicación host en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="5e509-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="5e509-151">Para obtener más información sobre cómo compilar el marcado del marco de cinta, consulte [compilar el marcado de cinta](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="5e509-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="5e509-152">Compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-152">Build the Application</span></span>

<span data-ttu-id="5e509-153">Una vez que la interfaz de usuario preliminar para una aplicación de cinta se ha diseñado e implementado en el marcado, debe escribirse código de aplicación que inicialice el marco de trabajo, consume el marcado y enlaza los comandos declarados en el marcado a los controladores de comandos adecuados en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5e509-154">Dado que el marco de la cinta de opciones está basado en COM, se recomienda que los proyectos de la cinta de opciones utilicen el \_ \_ operador uuidof () para hacer referencia a los GUID de las interfaces del marco de cinta (IID).</span><span class="sxs-lookup"><span data-stu-id="5e509-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="5e509-155">En aquellos casos en los que no es posible usar el \_ \_ operador uuidof (), como cuando se usa un compilador que no es de Microsoft o la aplicación host se basa en C, la aplicación debe definir los IID, ya que no están incluidos en UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="5e509-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="5e509-156">Si la aplicación define los IID, se deben usar los GUID especificados en UIRibbon. idl.</span><span class="sxs-lookup"><span data-stu-id="5e509-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="5e509-157">UIRibbon. idl se incluye como parte del [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx) y puede encontrarse en la ruta de instalación estándar de% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.</span><span class="sxs-lookup"><span data-stu-id="5e509-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="5e509-158">Inicializar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="5e509-158">Initialize the Ribbon</span></span>

<span data-ttu-id="5e509-159">En el diagrama siguiente se muestran los pasos necesarios para implementar una aplicación de cinta de opciones simple.</span><span class="sxs-lookup"><span data-stu-id="5e509-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![diagrama que muestra los pasos necesarios para implementar una implementación de cinta de opciones simple.](images/overviews/initializationsteps.png)

<span data-ttu-id="5e509-161">En los pasos siguientes se describe en detalle cómo implementar una aplicación de cinta de opciones simple.</span><span class="sxs-lookup"><span data-stu-id="5e509-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="5e509-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="5e509-162">CoCreateInstance</span></span>

    <span data-ttu-id="5e509-163">La aplicación llama a la función CoCreateInstance de COM estándar con el identificador de clase de marco de cinta para obtener un puntero al marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5e509-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="5e509-164">Initialize (HWND, IUIApplication \* )</span><span class="sxs-lookup"><span data-stu-id="5e509-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="5e509-165">La aplicación llama a [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), pasando dos parámetros: el identificador de la ventana de nivel superior que contendrá la cinta de opciones y un puntero a la implementación de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite que el marco de trabajo realice devoluciones de llamada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="5e509-166">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="5e509-166">\[!Important\]</span></span>  
    > <span data-ttu-id="5e509-167">El marco de la cinta de opciones se inicializa como un contenedor uniproceso (STA).</span><span class="sxs-lookup"><span data-stu-id="5e509-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="5e509-168">LoadUI (instancia, resourceName)</span><span class="sxs-lookup"><span data-stu-id="5e509-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="5e509-169">La aplicación llama a [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para enlazar el recurso de marcado.</span><span class="sxs-lookup"><span data-stu-id="5e509-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="5e509-170">El primer parámetro de esta función es un identificador de la instancia de la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="5e509-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="5e509-171">El segundo parámetro es el nombre del recurso de marcado binario que se compiló anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5e509-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="5e509-172">Al pasar el marcado binario al marco de la cinta de opciones, la aplicación indica cuál debe ser la estructura de la cinta y cómo deben organizarse los controles.</span><span class="sxs-lookup"><span data-stu-id="5e509-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="5e509-173">También proporciona el marco de trabajo con un manifiesto de comandos para exponer (como pegar, cortar, buscar), que usa el marco de trabajo cuando realiza devoluciones de llamada relacionadas con el comando en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5e509-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="5e509-174">Devoluciones de llamada [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)</span><span class="sxs-lookup"><span data-stu-id="5e509-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="5e509-175">Una vez completados los pasos del 1 al 3, el marco de la cinta de opciones sabe qué comandos exponer en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="5e509-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="5e509-176">Sin embargo, el marco sigue necesitando dos cosas antes de que la cinta sea totalmente funcional: una manera de indicar a la aplicación Cuándo se ejecutan los comandos y una manera de obtener recursos de comando o propiedades en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5e509-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="5e509-177">Por ejemplo, si un cuadro combinado va a aparecer en la interfaz de usuario, el marco de trabajo debe solicitar los elementos con los que rellenar el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="5e509-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="5e509-178">Estos dos fragmentos de funcionalidad se controlan a través de la interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="5e509-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="5e509-179">En concreto, para cada comando declarado en el marcado binario (vea el paso 3 anterior), el marco llama a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) para solicitar a la aplicación un objeto **IUICommandHandler** para ese comando.</span><span class="sxs-lookup"><span data-stu-id="5e509-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="5e509-180">La interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite enlazar un controlador de comandos a uno o varios comandos.</span><span class="sxs-lookup"><span data-stu-id="5e509-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="5e509-181">Como mínimo, la aplicación debe implementar los códigos auxiliares de los métodos [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que devuelven E \_ NOTIMPL como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e509-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="5e509-182">Vincular el marcado a la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-182">Link the Markup to the Application</span></span>

<span data-ttu-id="5e509-183">En este momento, los archivos de recursos de marcado deben estar vinculados a la aplicación host mediante la inclusión de una referencia al archivo de definición de recursos de marcado (que contiene una referencia al archivo de encabezado de marcado) en el archivo de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="5e509-184">Por ejemplo, una aplicación denominada RibbonApp con un archivo de recursos denominado ribbonUI. RC requiere la siguiente línea en el archivo RibbonApp. rc.</span><span class="sxs-lookup"><span data-stu-id="5e509-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="5e509-185">Dependiendo del compilador y del vinculador que se use, es posible que el script de definición de recursos también requiera la compilación antes de que se pueda compilar la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="5e509-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="5e509-186">La herramienta de línea de comandos [del compilador de recursos (RC)](../menurc/using-rc-the-rc-command-line-.md) que se incluye con Microsoft Visual Studio y el Windows SDK se puede usar para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="5e509-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="5e509-187">Compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e509-187">Compile the Application</span></span>

<span data-ttu-id="5e509-188">Una vez compilada la aplicación de cinta, se puede ejecutar y se ha probado la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e509-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="5e509-189">Si la interfaz de usuario requiere la modificación y no hay ningún cambio en los controladores de comandos asociados en el código de aplicación principal, revise el archivo de código fuente de marcado, vuelva a compilar el marcado con UICC.exe y vincule los nuevos archivos de recursos de marcado.</span><span class="sxs-lookup"><span data-stu-id="5e509-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="5e509-190">Cuando se reinicia la aplicación, se muestra la interfaz de usuario modificada.</span><span class="sxs-lookup"><span data-stu-id="5e509-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="5e509-191">Todo esto es posible sin tocar el código de aplicación principal, una mejora significativa sobre el desarrollo y la distribución de aplicaciones estándar.</span><span class="sxs-lookup"><span data-stu-id="5e509-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="5e509-192">Actualizaciones y ejecuciones en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5e509-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="5e509-193">La estructura de comunicación en tiempo de ejecución del marco de la cinta de opciones se basa en un modelo de llamador de inserción y extracción, o de llamada bidireccional.</span><span class="sxs-lookup"><span data-stu-id="5e509-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="5e509-194">Este modelo permite que el marco de trabajo informe a la aplicación cuando se ejecuta un comando y permite que el marco y la aplicación consulten, actualicen e invaliden los valores de propiedad y los recursos de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="5e509-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="5e509-195">Esta funcionalidad se proporciona a través de una serie de interfaces y métodos.</span><span class="sxs-lookup"><span data-stu-id="5e509-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="5e509-196">El marco extrae información de propiedades actualizada de la aplicación de cinta a través del método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="5e509-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="5e509-197">Un identificador de comando y una clave de propiedad, que identifica la propiedad de comando que se va a actualizar, se pasan al método que devuelve, o inserciones, un valor para esa clave de propiedad en el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5e509-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="5e509-198">El marco de trabajo llama a [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se ejecuta un comando, que identifica el identificador de comando y el tipo de ejecución que se ha producido ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span><span class="sxs-lookup"><span data-stu-id="5e509-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="5e509-199">Aquí es donde la aplicación especifica la lógica de ejecución de un comando.</span><span class="sxs-lookup"><span data-stu-id="5e509-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="5e509-200">En el diagrama siguiente se muestra la comunicación en tiempo de ejecución para la ejecución de comandos entre el marco de trabajo y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![diagrama que muestra un ejemplo de la comunicación en tiempo de ejecución entre el marco de la cinta de opciones y una aplicación host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="5e509-202">No es necesario implementar las funciones [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para mostrar inicialmente una cinta en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="5e509-203">Sin embargo, estos métodos son necesarios para garantizar que la aplicación funciona correctamente cuando el usuario ejecuta los comandos.</span><span class="sxs-lookup"><span data-stu-id="5e509-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="5e509-204">Compatibilidad con OLE</span><span class="sxs-lookup"><span data-stu-id="5e509-204">OLE Support</span></span>

<span data-ttu-id="5e509-205">Una aplicación de la cinta de opciones se puede configurar como un servidor OLE para admitir la activación OLE fuera de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="5e509-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="5e509-206">Los objetos creados en una aplicación de servidor OLE mantienen su asociación con la aplicación de servidor cuando se insertan (se pegan o colocan) en una aplicación cliente OLE (o contenedor).</span><span class="sxs-lookup"><span data-stu-id="5e509-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="5e509-207">En la activación OLE fuera de la ubicación, al hacer doble clic en el objeto en la aplicación cliente, se abre una instancia dedicada de la aplicación de servidor y se carga el objeto para su edición.</span><span class="sxs-lookup"><span data-stu-id="5e509-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="5e509-208">Cuando se cierra la aplicación de servidor, todos los cambios realizados en el objeto se reflejan en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5e509-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="5e509-209">El marco de la cinta de opciones no admite la activación OLE en contexto.</span><span class="sxs-lookup"><span data-stu-id="5e509-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="5e509-210">Los objetos creados en un servidor OLE basado en cinta no se pueden editar desde la aplicación cliente OLE.</span><span class="sxs-lookup"><span data-stu-id="5e509-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="5e509-211">Se requiere una instancia externa dedicada de la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="5e509-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="5e509-212">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e509-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e509-213">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="5e509-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="5e509-214">Instrucciones para la experiencia del usuario en cinta</span><span class="sxs-lookup"><span data-stu-id="5e509-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="5e509-215">Proceso de diseño de la cinta</span><span class="sxs-lookup"><span data-stu-id="5e509-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




