---
title: Trabajar con galerías
description: El marco de la cinta de opciones de Windows proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en una variedad de controles basados en colecciones.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Cinta de opciones de Windows, galerías
- Cinta de opciones, galerías
- Cinta de Windows, control DropDownGallery
- Cinta de opciones, control DropDownGallery
- Cinta de Windows, control SplitButtonGallery
- Cinta de opciones, control SplitButtonGallery
- Control DropDownGallery
- Control SplitButtonGallery
- galerías de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793072"
---
# <a name="working-with-galleries"></a><span data-ttu-id="b510e-112">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="b510e-112">Working with Galleries</span></span>

<span data-ttu-id="b510e-113">El marco de la cinta de opciones de Windows proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en una variedad de controles basados en colecciones.</span><span class="sxs-lookup"><span data-stu-id="b510e-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="b510e-114">Al adaptar y volver a configurar la interfaz de usuario de la cinta de opciones, estos controles dinámicos permiten que el marco de trabajo responda a la interacción del usuario en la propia cinta y la aplicación host, y proporciona la flexibilidad necesaria para controlar diversos entornos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b510e-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="b510e-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="b510e-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b510e-116">Galerías</span><span class="sxs-lookup"><span data-stu-id="b510e-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="b510e-117">Galerías de elementos</span><span class="sxs-lookup"><span data-stu-id="b510e-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="b510e-118">Galerías de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="b510e-119">Controles de la galería</span><span class="sxs-lookup"><span data-stu-id="b510e-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="b510e-120">Cómo implementar una galería</span><span class="sxs-lookup"><span data-stu-id="b510e-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="b510e-121">Componentes básicos</span><span class="sxs-lookup"><span data-stu-id="b510e-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="b510e-122">Declarar los controles en el marcado</span><span class="sxs-lookup"><span data-stu-id="b510e-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="b510e-123">Crear un controlador de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="b510e-124">Enlazar el controlador de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="b510e-125">Inicializar una colección</span><span class="sxs-lookup"><span data-stu-id="b510e-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="b510e-126">Controlar eventos de colección</span><span class="sxs-lookup"><span data-stu-id="b510e-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="b510e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b510e-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b510e-128">Introducción</span><span class="sxs-lookup"><span data-stu-id="b510e-128">Introduction</span></span>

<span data-ttu-id="b510e-129">Esta capacidad del marco de cinta para adaptarse dinámicamente a las condiciones de tiempo de ejecución, los requisitos de la aplicación y los datos proporcionados por el usuario final resalta las amplias capacidades de la interfaz de usuario del marco de trabajo y ofrece a los desarrolladores la flexibilidad de satisfacer una amplia gama de necesidades del cliente.</span><span class="sxs-lookup"><span data-stu-id="b510e-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="b510e-130">El objetivo de esta guía es describir los controles dinámicos de la Galería admitidos por el marco, explicar sus diferencias, comentar Cuándo y dónde se pueden usar mejor y demostrar cómo se pueden incorporar en una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="b510e-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="b510e-131">Galerías</span><span class="sxs-lookup"><span data-stu-id="b510e-131">Galleries</span></span>

<span data-ttu-id="b510e-132">Las galerías son controles de cuadro de lista de forma funcional y gráficamente enriquecidos.</span><span class="sxs-lookup"><span data-stu-id="b510e-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="b510e-133">La colección de elementos de una galería se puede organizar por categorías, que se muestra en diseños flexibles basados en filas y columnas, representados con imágenes y texto, y en función del tipo de galería, admiten la vista previa en vivo.</span><span class="sxs-lookup"><span data-stu-id="b510e-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="b510e-134">Las galerías son funcionalmente distintas de otros controles dinámicos de la cinta de opciones por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="b510e-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="b510e-135">Las galerías implementan la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) que define los distintos métodos para manipular colecciones de elementos de la galería.</span><span class="sxs-lookup"><span data-stu-id="b510e-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="b510e-136">Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce directamente en la cinta de opciones, por ejemplo, cuando un usuario agrega un comando a la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="b510e-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="b510e-137">Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente desde el entorno de tiempo de ejecución, por ejemplo, cuando un controlador de impresora solo admite diseños de página verticales.</span><span class="sxs-lookup"><span data-stu-id="b510e-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="b510e-138">Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente en la aplicación host, como cuando un usuario selecciona un elemento en un documento.</span><span class="sxs-lookup"><span data-stu-id="b510e-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="b510e-139">El marco de la cinta de opciones expone dos tipos de galerías: galerías de elementos y galerías de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="b510e-140">Galerías de elementos</span><span class="sxs-lookup"><span data-stu-id="b510e-140">Item Galleries</span></span>

<span data-ttu-id="b510e-141">Las galerías de elementos contienen una colección basada en índices de elementos relacionados en la que cada elemento se representa mediante una imagen, una cadena o ambos.</span><span class="sxs-lookup"><span data-stu-id="b510e-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="b510e-142">El control está enlazado a un controlador de comandos único que se basa en el valor de índice identificado por la propiedad PKEY de la [interfaz de usuario \_ \_ ](windowsribbon-reference-properties-uipkey-selecteditem.md) .</span><span class="sxs-lookup"><span data-stu-id="b510e-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="b510e-143">Las galerías de elementos admiten la vista previa en directo, lo que significa que se muestra el resultado de un comando, basado en mouseover o Focus, sin confirmar ni invocar realmente el comando.</span><span class="sxs-lookup"><span data-stu-id="b510e-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b510e-144">El marco de trabajo no admite galerías de elementos de hospedaje en el menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b510e-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="b510e-145">Galerías de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-145">Command Galleries</span></span>

<span data-ttu-id="b510e-146">Las galerías de comandos contienen una colección de elementos distintos que no están indexados.</span><span class="sxs-lookup"><span data-stu-id="b510e-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="b510e-147">Cada elemento se representa mediante un único control enlazado a un controlador de comandos a través de un identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="b510e-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="b510e-148">Al igual que los controles independientes, cada elemento de una galería de comandos enruta los eventos de entrada a un controlador de comandos asociado; la galería de comandos no realiza escuchas de eventos.</span><span class="sxs-lookup"><span data-stu-id="b510e-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="b510e-149">Las galerías de comandos no admiten la vista previa dinámica.</span><span class="sxs-lookup"><span data-stu-id="b510e-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="b510e-150">Controles de la galería</span><span class="sxs-lookup"><span data-stu-id="b510e-150">Gallery Controls</span></span>

<span data-ttu-id="b510e-151">Hay cuatro controles de galería en el marco de la cinta de opciones: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)y [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="b510e-152">Todo excepto el **cuadro combinado** se puede implementar como una galería de elementos o una galería de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="b510e-153">DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="b510e-153">DropDownGallery</span></span>

<span data-ttu-id="b510e-154">Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) es un botón que muestra una lista desplegable que contiene una colección de elementos o comandos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="b510e-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="b510e-155">En la captura de pantalla siguiente se muestra el control [Galería desplegable](windowsribbon-controls-dropdowngallery.md) de la cinta de opciones de Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b510e-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de Galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="b510e-157">SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="b510e-157">SplitButtonGallery</span></span>

<span data-ttu-id="b510e-158">Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) es un control compuesto que expone un único elemento o Comando predeterminado de su colección en un botón principal y muestra otros elementos o comandos en una lista desplegable mutuamente excluyente que se muestra cuando se hace clic en un botón secundario.</span><span class="sxs-lookup"><span data-stu-id="b510e-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="b510e-159">En la captura de pantalla siguiente se muestra el control [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md) de la cinta en Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b510e-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control Galería de botones de división en Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="b510e-161">InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="b510e-161">InRibbonGallery</span></span>

<span data-ttu-id="b510e-162">Un [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) es una galería que muestra una colección de elementos o comandos relacionados en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b510e-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="b510e-163">Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.</span><span class="sxs-lookup"><span data-stu-id="b510e-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="b510e-164">En la captura de pantalla siguiente se muestra el control [Galería de cintas en cinta](windowsribbon-controls-inribbongallery.md) de opciones de Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b510e-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de la galería de la cinta de opciones en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="b510e-166">ComboBox</span><span class="sxs-lookup"><span data-stu-id="b510e-166">ComboBox</span></span>

<span data-ttu-id="b510e-167">Un cuadro [**combinado**](windowsribbon-element-combobox.md) es un cuadro de lista de una sola columna que contiene una colección de elementos con un control estático o un control de edición y una flecha de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="b510e-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="b510e-168">La parte del cuadro de lista del control se muestra cuando el usuario hace clic en la flecha de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="b510e-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="b510e-169">En la captura de pantalla siguiente se muestra un control de [cuadro combinado](windowsribbon-controls-combobox.md) de la cinta de opciones de Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="b510e-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![captura de pantalla de un control ComboBox en la cinta de opciones de Microsoft Paint.](images/controls/combobox.png)

<span data-ttu-id="b510e-171">Dado que el [**cuadro combinado**](windowsribbon-element-combobox.md) es exclusivamente una galería de elementos, no admite elementos de comando.</span><span class="sxs-lookup"><span data-stu-id="b510e-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="b510e-172">También es el único control de la galería que no admite un espacio de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="b510e-173">(Un espacio de comandos es una colección de comandos que se declaran en el marcado y que se enumeran en la parte inferior de una galería de elementos o de una galería de comandos).</span><span class="sxs-lookup"><span data-stu-id="b510e-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="b510e-174">En el ejemplo de código siguiente se muestra el marcado necesario para declarar un espacio de comandos de tres botones en un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="b510e-175">En la captura de pantalla siguiente se muestra el espacio de comandos de tres botones del ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="b510e-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![captura de pantalla de un espacio de comandos de tres botones en un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="b510e-177">Cómo implementar una galería</span><span class="sxs-lookup"><span data-stu-id="b510e-177">How to Implement a Gallery</span></span>

<span data-ttu-id="b510e-178">En esta sección se describen los detalles de implementación de las galerías de la cinta de opciones y se explica cómo incorporarlas en una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="b510e-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="b510e-179">Componentes básicos</span><span class="sxs-lookup"><span data-stu-id="b510e-179">The Basic Components</span></span>

<span data-ttu-id="b510e-180">En esta sección se describe el conjunto de propiedades y métodos que forman la red troncal de contenido dinámico en el marco de la cinta de opciones y permiten agregar, eliminar, actualizar y, de otro modo, manipular el contenido y el diseño visual de las galerías de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b510e-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="b510e-181">IUICollection</span><span class="sxs-lookup"><span data-stu-id="b510e-181">IUICollection</span></span>

<span data-ttu-id="b510e-182">Las galerías requieren un conjunto básico de métodos para tener acceso a los elementos individuales de sus colecciones y manipularlos.</span><span class="sxs-lookup"><span data-stu-id="b510e-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="b510e-183">La interfaz [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) define estos métodos y el marco complementa su funcionalidad con métodos adicionales que se definen en la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="b510e-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="b510e-184">El marco de trabajo implementa **IUICollection** para cada declaración de galería en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b510e-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="b510e-185">Si se requiere una funcionalidad adicional que no proporciona la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , un objeto de colección personalizado implementado por la aplicación host y derivado de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) se puede sustituir por la colección de Framework.</span><span class="sxs-lookup"><span data-stu-id="b510e-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="b510e-186">IUICollectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="b510e-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="b510e-187">Para que una aplicación responda a los cambios de una colección de la galería, debe implementar la interfaz [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) .</span><span class="sxs-lookup"><span data-stu-id="b510e-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="b510e-188">Las aplicaciones se pueden suscribir a notificaciones desde un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través del agente de escucha de eventos [**IUICollectionChangedEvent:: alchanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="b510e-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="b510e-189">Cuando la aplicación reemplaza la colección de la Galería proporcionada por el marco de trabajo por una colección personalizada, la aplicación debe implementar la interfaz [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .</span><span class="sxs-lookup"><span data-stu-id="b510e-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="b510e-190">Si no se implementa [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) , la aplicación no puede notificar a la plataforma los cambios en la colección personalizada que requieren actualizaciones dinámicas en el control de la galería.</span><span class="sxs-lookup"><span data-stu-id="b510e-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="b510e-191">En aquellos casos en los que no se implementa [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) , el control de Galería solo se puede actualizar mediante invalidación a través de [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) y [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), o bien mediante una llamada a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="b510e-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="b510e-192">IUISimplePropertySet</span><span class="sxs-lookup"><span data-stu-id="b510e-192">IUISimplePropertySet</span></span>

<span data-ttu-id="b510e-193">Las aplicaciones deben implementar IUISimplePropertySet para cada elemento o comando de una colección de la galería.</span><span class="sxs-lookup"><span data-stu-id="b510e-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="b510e-194">Sin embargo, las propiedades que se pueden solicitar con [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) varían.</span><span class="sxs-lookup"><span data-stu-id="b510e-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="b510e-195">Los elementos se definen y se enlazan a una galería a través de la clave de la propiedad [ \_ \_ PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) de la interfaz de usuario y exponen las propiedades con un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="b510e-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="b510e-196">Las propiedades válidas para los elementos de las galerías de elementos ([**\_ \_ colección COMMANDTYPE de UI**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b510e-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="b510e-197">Algunas propiedades de elemento, como [la \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario, se pueden definir en el marcado.</span><span class="sxs-lookup"><span data-stu-id="b510e-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="b510e-198">Para obtener más información, consulte la documentación de referencia de [las claves de propiedad](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="b510e-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="b510e-199">Control</span><span class="sxs-lookup"><span data-stu-id="b510e-199">Control</span></span>

<span data-ttu-id="b510e-200">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b510e-200">Properties</span></span>

[<span data-ttu-id="b510e-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="b510e-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="b510e-202">[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b510e-203">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="b510e-204">[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b510e-205">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="b510e-206">[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b510e-207">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="b510e-208">[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="b510e-209">[Interfaz de usuario \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) es una propiedad de la galería de elementos.</span><span class="sxs-lookup"><span data-stu-id="b510e-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="b510e-210">En la tabla siguiente se describen las propiedades válidas de los elementos de las galerías de comandos ([**\_ \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="b510e-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="b510e-211">Control</span><span class="sxs-lookup"><span data-stu-id="b510e-211">Control</span></span>                                                                | <span data-ttu-id="b510e-212">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b510e-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b510e-213">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="b510e-214">[Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="b510e-215">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="b510e-216">[Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="b510e-217">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b510e-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="b510e-218">[Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b510e-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="b510e-219">Las categorías se utilizan para organizar elementos y comandos en galerías.</span><span class="sxs-lookup"><span data-stu-id="b510e-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="b510e-220">Las categorías se definen y se enlazan a una galería a través de la clave de propiedad de la [interfaz de usuario \_ PKEY \_ categorías](windowsribbon-reference-properties-uipkey-categories.md) y exponen las propiedades con un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) específico de la categoría.</span><span class="sxs-lookup"><span data-stu-id="b510e-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="b510e-221">Las categorías no tienen un CommandType y no admiten la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="b510e-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="b510e-222">Por ejemplo, las categorías no se pueden convertir en SelectedItem en una galería de elementos y no están enlazadas a un comando en una galería de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="b510e-223">Al igual que otras propiedades de elementos de la galería, las propiedades de categoría como la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md) de la interfaz de usuario y la [interfaz de usuario \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) se pueden recuperar llamando a [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span><span class="sxs-lookup"><span data-stu-id="b510e-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b510e-224">[**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) debe devolver la [**colección de interfaz de usuario \_ \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) cuando se solicita la [interfaz de usuario \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) para un elemento que no tiene una categoría asociada.</span><span class="sxs-lookup"><span data-stu-id="b510e-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="b510e-225">Declarar los controles en el marcado</span><span class="sxs-lookup"><span data-stu-id="b510e-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="b510e-226">Las galerías, como todos los controles de la cinta de opciones, se deben declarar en el marcado.</span><span class="sxs-lookup"><span data-stu-id="b510e-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="b510e-227">Una galería se identifica en el marcado como una galería de elementos o una galería de comandos y se declaran varios detalles de presentación.</span><span class="sxs-lookup"><span data-stu-id="b510e-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="b510e-228">A diferencia de otros controles, las galerías solo requieren el control base o el contenedor de la colección para que se declaren en el marcado.</span><span class="sxs-lookup"><span data-stu-id="b510e-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="b510e-229">Las colecciones reales se rellenan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b510e-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="b510e-230">Cuando se declara una galería en el marcado, el atributo de *tipo* se usa para especificar si la Galería es una galería de elementos de una galería de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="b510e-231">Hay una serie de atributos de diseño opcionales disponibles para cada uno de los controles que se describen aquí.</span><span class="sxs-lookup"><span data-stu-id="b510e-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="b510e-232">Estos atributos proporcionan preferencias de desarrollador para que el marco de trabajo siga que afectan directamente a cómo se rellena y se muestra un control en una cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b510e-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="b510e-233">Las preferencias aplicables en el marcado están relacionadas con las plantillas de presentación y diseño, y los comportamientos descritos en [Personalización de una cinta a través de las definiciones de tamaño y las directivas de escalado](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="b510e-234">Si un control determinado no permite las preferencias de diseño directamente en el marcado o no se especifican las preferencias de diseño, el marco de trabajo define las convenciones de presentación específicas del control en función de la cantidad de espacio en pantalla disponible.</span><span class="sxs-lookup"><span data-stu-id="b510e-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="b510e-235">En los siguientes ejemplos se muestra cómo incorporar un conjunto de galerías en una cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b510e-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="b510e-236">Declaraciones de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-236">Command Declarations</span></span>

<span data-ttu-id="b510e-237">Los comandos se deben declarar con un atributo *CommandName* que se utiliza para asociar un control o un conjunto de controles con el comando.</span><span class="sxs-lookup"><span data-stu-id="b510e-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="b510e-238">Un atributo *CommandID* que se usa para enlazar un comando a un controlador de comandos cuando se compila el marcado también se puede especificar aquí.</span><span class="sxs-lookup"><span data-stu-id="b510e-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="b510e-239">Si no se proporciona ningún identificador, el marco de trabajo genera uno.</span><span class="sxs-lookup"><span data-stu-id="b510e-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="b510e-240">Declaraciones de control</span><span class="sxs-lookup"><span data-stu-id="b510e-240">Control Declarations</span></span>

<span data-ttu-id="b510e-241">Esta sección contiene ejemplos que muestran el marcado de control básico necesario para los distintos tipos de galería.</span><span class="sxs-lookup"><span data-stu-id="b510e-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="b510e-242">Muestran cómo declarar los controles de la galería y asociarlos con un comando mediante el atributo *CommandName* .</span><span class="sxs-lookup"><span data-stu-id="b510e-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="b510e-243">En el ejemplo siguiente se muestra una declaración de control para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) donde se usa el atributo *Type* para especificar que se trata de una galería de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="b510e-244">En el ejemplo siguiente se muestra una declaración de control para [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="b510e-245">En el ejemplo siguiente se muestra una declaración de control para [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="b510e-246">Dado que [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) está diseñado para mostrar un subconjunto de su colección de elementos en la cinta de opciones sin activar un menú desplegable, proporciona una serie de atributos opcionales que rigen su tamaño y diseño de elemento en la inicialización de la cinta.</span><span class="sxs-lookup"><span data-stu-id="b510e-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="b510e-247">Estos atributos son exclusivos de **InRibbonGallery** y no están disponibles en los demás controles dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b510e-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="b510e-248">En el ejemplo siguiente se muestra una declaración de control para el [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="b510e-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="b510e-249">Crear un controlador de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-249">Create a Command Handler</span></span>

<span data-ttu-id="b510e-250">Para cada comando, el marco de la cinta de opciones requiere un controlador de comandos correspondiente en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="b510e-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="b510e-251">Los controladores de comandos se implementan mediante la aplicación host de la cinta de opciones y se derivan de la interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="b510e-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="b510e-252">Se pueden enlazar varios comandos a un solo controlador de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="b510e-253">Un controlador de comandos sirve para dos propósitos:</span><span class="sxs-lookup"><span data-stu-id="b510e-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="b510e-254">[**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responde a las solicitudes de actualización de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b510e-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="b510e-255">Los valores de las propiedades del comando, como la [interfaz de usuario \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario, se establecen a través de llamadas a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="b510e-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="b510e-256">[**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responde a los eventos de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b510e-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="b510e-257">Este método admite los siguientes tres Estados de ejecución especificados por el [**parámetro \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b510e-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="b510e-258">El estado de ejecución ejecuta, o confirma, los comandos a los que está enlazado el controlador.</span><span class="sxs-lookup"><span data-stu-id="b510e-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="b510e-259">El estado de vista previa muestra una vista previa de los comandos a los que está enlazado el controlador.</span><span class="sxs-lookup"><span data-stu-id="b510e-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="b510e-260">En esencia, se ejecutan los comandos sin confirmar el resultado.</span><span class="sxs-lookup"><span data-stu-id="b510e-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="b510e-261">El estado CancelPreview cancela los comandos de vista previa.</span><span class="sxs-lookup"><span data-stu-id="b510e-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="b510e-262">Esto es necesario para admitir el recorrido a través de un menú o una lista, y la vista previa secuencial y deshacer los resultados según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b510e-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="b510e-263">En el ejemplo siguiente se muestra un controlador de comandos de la galería.</span><span class="sxs-lookup"><span data-stu-id="b510e-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="b510e-264">Enlazar el controlador de comandos</span><span class="sxs-lookup"><span data-stu-id="b510e-264">Bind the Command Handler</span></span>

<span data-ttu-id="b510e-265">Después de definir un controlador de comandos, el comando debe estar enlazado al controlador.</span><span class="sxs-lookup"><span data-stu-id="b510e-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="b510e-266">En el ejemplo siguiente se muestra cómo enlazar un comando de la galería a un controlador de comandos específico.</span><span class="sxs-lookup"><span data-stu-id="b510e-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="b510e-267">En este caso, los controles [**ComboBox**](windowsribbon-element-combobox.md) y Gallery se enlazan a sus controladores de comandos respectivos.</span><span class="sxs-lookup"><span data-stu-id="b510e-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="b510e-268">Inicializar una colección</span><span class="sxs-lookup"><span data-stu-id="b510e-268">Initialize a Collection</span></span>

<span data-ttu-id="b510e-269">En el ejemplo siguiente se muestra una implementación personalizada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para las galerías de elementos y de comandos.</span><span class="sxs-lookup"><span data-stu-id="b510e-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="b510e-270">La clase CItemProperties de este ejemplo se deriva de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span><span class="sxs-lookup"><span data-stu-id="b510e-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="b510e-271">Además del método necesario [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), la clase CItemProperties implementa un conjunto de funciones auxiliares para la inicialización y el seguimiento de índices.</span><span class="sxs-lookup"><span data-stu-id="b510e-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="b510e-272">Controlar eventos de colección</span><span class="sxs-lookup"><span data-stu-id="b510e-272">Handle Collection Events</span></span>

<span data-ttu-id="b510e-273">En el ejemplo siguiente se muestra una implementación de IUICollectionChangedEvent.</span><span class="sxs-lookup"><span data-stu-id="b510e-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="b510e-274">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b510e-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b510e-275">Propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="b510e-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="b510e-276">Crear una aplicación de cinta</span><span class="sxs-lookup"><span data-stu-id="b510e-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="b510e-277">Descripción de los comandos y los controles</span><span class="sxs-lookup"><span data-stu-id="b510e-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="b510e-278">Instrucciones para la experiencia del usuario en cinta</span><span class="sxs-lookup"><span data-stu-id="b510e-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="b510e-279">Proceso de diseño de la cinta</span><span class="sxs-lookup"><span data-stu-id="b510e-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="b510e-280">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="b510e-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 