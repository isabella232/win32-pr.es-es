---
title: Declarar comandos y controles con el marcado de la cinta de opciones
description: El marco de cinta de Windows usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar de forma declarativa la apariencia de una aplicación de cinta.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Cinta de Windows, estructura de marcado
- Cinta, estructura de marcado
- Cinta de opciones de Windows, separar la presentación de la lógica de comandos
- Cinta de opciones, separar la presentación de la lógica de comandos
- Cinta de Windows, componentes
- Cinta de opciones, componentes
- sistema de comandos para la cinta de Windows
- controles de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421136"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="5598d-111">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="5598d-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="5598d-112">El marco de cinta de Windows usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar de forma declarativa la apariencia de una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="5598d-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="5598d-113">Separar la presentación de la lógica de comandos</span><span class="sxs-lookup"><span data-stu-id="5598d-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="5598d-114">Estructura de marcado</span><span class="sxs-lookup"><span data-stu-id="5598d-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="5598d-115">Componentes de la cinta</span><span class="sxs-lookup"><span data-stu-id="5598d-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="5598d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5598d-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="5598d-117">Separar la presentación de la lógica de comandos</span><span class="sxs-lookup"><span data-stu-id="5598d-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="5598d-118">La separación de los atributos visuales y de presentación de la lógica de comandos en el marco de cinta se realiza a través de dos plataformas de desarrollo distintas, pero dependientes.</span><span class="sxs-lookup"><span data-stu-id="5598d-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="5598d-119">Los diseños de control, los comportamientos de escalado, las declaraciones de comandos y las especificaciones de recursos son el dominio de tiempo de diseño de una sintaxis de marcado declarativo basada en la especificación [lenguaje XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) .</span><span class="sxs-lookup"><span data-stu-id="5598d-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="5598d-120">En las implementaciones de interfaz basadas en el modelo de objetos componentes (COM) se definen la funcionalidad de bajo nivel, los enlaces de aplicación y los controladores de comandos.</span><span class="sxs-lookup"><span data-stu-id="5598d-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="5598d-121">Esta separación de la presentación y la lógica proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="5598d-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="5598d-122">Un ciclo de desarrollo de aplicaciones más eficaz que permite a los desarrolladores y diseñadores de la interfaz de usuario implementar la GUI de la aplicación de cinta independientemente de la funcionalidad básica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5598d-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="5598d-123">Esta funcionalidad principal se puede dejar a los desarrolladores de software dedicados.</span><span class="sxs-lookup"><span data-stu-id="5598d-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="5598d-124">Mantenimiento menos costoso porque los cambios en la interfaz gráfica de usuario son posibles sin cambios en la funcionalidad básica (y viceversa).</span><span class="sxs-lookup"><span data-stu-id="5598d-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="5598d-125">Especificación simple de los recursos de cadena e imagen mediante marcado.</span><span class="sxs-lookup"><span data-stu-id="5598d-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="5598d-126">Facilidad de prototipos.</span><span class="sxs-lookup"><span data-stu-id="5598d-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="5598d-127">Estructura de marcado</span><span class="sxs-lookup"><span data-stu-id="5598d-127">Markup Structure</span></span>

<span data-ttu-id="5598d-128">Existen dos ramas distintas dentro de la estructura del marcado del marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="5598d-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="5598d-129">La primera bifurcación contiene un manifiesto de declaraciones de comandos y recursos (cadenas e imágenes).</span><span class="sxs-lookup"><span data-stu-id="5598d-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="5598d-130">El marco de trabajo usa cada entrada de comando para enlazar un control de la cinta de opciones, a través de un identificador de comando, a un controlador de comandos definido en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5598d-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="5598d-131">La segunda bifurcación contiene las declaraciones de control reales.</span><span class="sxs-lookup"><span data-stu-id="5598d-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="5598d-132">Cada control está asociado a un comando a través de un atributo *CommandName* que se asigna a un atributo de *nombre* especificado en cada declaración de comando.</span><span class="sxs-lookup"><span data-stu-id="5598d-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="5598d-133">Componentes de la cinta</span><span class="sxs-lookup"><span data-stu-id="5598d-133">Ribbon Components</span></span>

<span data-ttu-id="5598d-134">La funcionalidad de la interfaz de usuario del marco de cinta se expone a través de [vistas](windowsribbon-reference-elements-view.md).</span><span class="sxs-lookup"><span data-stu-id="5598d-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="5598d-135">Una vista es esencialmente un contenedor, como la [**cinta**](windowsribbon-element-ribbon.md) de opciones y [**ContextPopup**](windowsribbon-element-contextpopup.md), que se usa para presentar controles de marco y los comandos a los que están enlazados.</span><span class="sxs-lookup"><span data-stu-id="5598d-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="5598d-136">La vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones se compone de varios componentes que incluyen un menú de la [aplicación](windowsribbon-controls-applicationmenu.md), la barra de [herramientas de acceso rápido (Qat)](windowsribbon-controls-quickaccesstoolbar.md) para mostrar los comandos usados habitualmente en la interfaz de usuario de la cinta de opciones, las [pestañas](windowsribbon-controls-tab.md) principal y contextual que contienen [grupos](windowsribbon-controls-group.md) de controles y el completo sistema de menús contextuales del [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="5598d-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="5598d-137">Todos los componentes de la cinta de opciones se declaran en un archivo de marcado independiente que:</span><span class="sxs-lookup"><span data-stu-id="5598d-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="5598d-138">Especifica las propiedades básicas de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="5598d-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="5598d-139">Muestra claramente las relaciones jerárquicas.</span><span class="sxs-lookup"><span data-stu-id="5598d-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="5598d-140">Proporciona las preferencias de diseño y las sugerencias de escalado.</span><span class="sxs-lookup"><span data-stu-id="5598d-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="5598d-141">Para obtener más información sobre las plantillas de diseño del marco de cinta, vea [personalizar una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="5598d-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="5598d-142">Proporciona una manera de definir recursos como imágenes y etiquetas.</span><span class="sxs-lookup"><span data-stu-id="5598d-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="5598d-143">Para obtener más información sobre los recursos de imagen, consulte [especificar recursos de imagen de la cinta](windowsribbon-imageformats.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="5598d-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="5598d-144">Los dos ejemplos de marcado de la cinta de opciones siguientes muestran cómo un conjunto de elementos de menú de la aplicación de cinta está asociado a un nombre y un identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="5598d-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="5598d-145">En esta sección se muestran las declaraciones de comandos necesarias para un menú de la aplicación con comandos básicos como nuevo, abrir y guardar.</span><span class="sxs-lookup"><span data-stu-id="5598d-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="5598d-146">En esta sección se muestran las declaraciones de control asociadas.</span><span class="sxs-lookup"><span data-stu-id="5598d-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="5598d-147">Cuando el marcado se compila con la herramienta del compilador de comandos de la interfaz de usuario (UICC), los nombres y los identificadores de comando se colocan en un archivo de encabezado usado por la aplicación host de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="5598d-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="5598d-148">El siguiente es un ejemplo de un archivo de encabezado generado por UICC.</span><span class="sxs-lookup"><span data-stu-id="5598d-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="5598d-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5598d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5598d-150">Lenguaje XAML (XAML)</span><span class="sxs-lookup"><span data-stu-id="5598d-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="5598d-151">Compilar marcado de cinta</span><span class="sxs-lookup"><span data-stu-id="5598d-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 