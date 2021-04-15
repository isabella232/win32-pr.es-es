---
title: Biblioteca de controles de Windows Ribbon Framework
description: En los temas incluidos en esta sección se describe el conjunto de controles que se incluyen con el marco de la cinta de opciones de Windows. Los controles que se muestran aquí son los objetos de interfaz de usuario de una cinta que exponen la funcionalidad del comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676453"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="b2e7a-104">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="b2e7a-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="b2e7a-105">En los temas incluidos en esta sección se describe el conjunto de controles que se incluyen con el marco de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="b2e7a-106">Los controles que se muestran aquí son los objetos de interfaz de usuario de una cinta que exponen la funcionalidad del comando.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="b2e7a-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="b2e7a-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b2e7a-108">Los controles</span><span class="sxs-lookup"><span data-stu-id="b2e7a-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="b2e7a-109">Controles básicos</span><span class="sxs-lookup"><span data-stu-id="b2e7a-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="b2e7a-110">Controles de contenedor</span><span class="sxs-lookup"><span data-stu-id="b2e7a-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="b2e7a-111">Controles especializados</span><span class="sxs-lookup"><span data-stu-id="b2e7a-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="b2e7a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e7a-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b2e7a-113">Introducción</span><span class="sxs-lookup"><span data-stu-id="b2e7a-113">Introduction</span></span>

<span data-ttu-id="b2e7a-114">El marco de cinta se compone de componentes como [pestañas](windowsribbon-controls-tab.md) y la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md), que funcionan conjuntamente para ofrecer una experiencia de interfaz de usuario enriquecida.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="b2e7a-115">De forma individual, estos componentes exponen distintos tipos de comandos para ofrecer a los clientes una experiencia organizada y predecible en todas las aplicaciones de la cinta.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="b2e7a-116">Por ejemplo, cada pestaña expone comandos relacionados con la creación y la actuación en partes específicas del contenido dentro del área de trabajo de la aplicación, mientras que el [menú aplicación](windowsribbon-controls-applicationmenu.md) expone la funcionalidad relacionada con un proyecto completo, como un documento, una imagen o una película completos.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="b2e7a-117">En este tema se proporciona una lista completa de los controles de la cinta de opciones e incluye una breve descripción de cada control, con vínculos a documentación más detallada cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="b2e7a-118">Los controles</span><span class="sxs-lookup"><span data-stu-id="b2e7a-118">The Controls</span></span>

<span data-ttu-id="b2e7a-119">El marco de cinta se compone de dos [vistas](windowsribbon-reference-elements-view.md): la vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones y la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e7a-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="b2e7a-120">Cada vista puede hospedar varios componentes que actúan como contenedores de presentación para todos los controles que el marco de trabajo representa y administra.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="b2e7a-121">La vista de [**cinta**](windowsribbon-element-ribbon.md) hospeda el elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , el elemento [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) y la barra de comandos de la cinta mientras la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) hospeda un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) o ambos.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="b2e7a-122">Cada control de marco de trabajo se distingue por la funcionalidad asociada a su [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span><span class="sxs-lookup"><span data-stu-id="b2e7a-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="b2e7a-123">Controles básicos</span><span class="sxs-lookup"><span data-stu-id="b2e7a-123">Basic Controls</span></span>

<span data-ttu-id="b2e7a-124">Los controles básicos se componen de uno o varios botones que se pueden invocar mediante un solo clic del mouse para realizar una acción simple.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="b2e7a-125">El control de [**número**](windowsribbon-element-spinner.md) es una excepción, ya que contiene un control de edición.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="b2e7a-126">En la tabla siguiente se enumeran los controles básicos en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="b2e7a-127">Control</span><span class="sxs-lookup"><span data-stu-id="b2e7a-127">Control</span></span>                                                  | <span data-ttu-id="b2e7a-128">Elemento de marcado</span><span class="sxs-lookup"><span data-stu-id="b2e7a-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="b2e7a-129">Botón</span><span class="sxs-lookup"><span data-stu-id="b2e7a-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="b2e7a-130">**Botón**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="b2e7a-131">Casilla de verificación</span><span class="sxs-lookup"><span data-stu-id="b2e7a-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="b2e7a-132">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="b2e7a-133">Botón ayuda</span><span class="sxs-lookup"><span data-stu-id="b2e7a-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="b2e7a-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="b2e7a-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="b2e7a-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="b2e7a-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="b2e7a-137">Botón de alternancia</span><span class="sxs-lookup"><span data-stu-id="b2e7a-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="b2e7a-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="b2e7a-139">Controles de contenedor</span><span class="sxs-lookup"><span data-stu-id="b2e7a-139">Container Controls</span></span>

<span data-ttu-id="b2e7a-140">Los controles de contenedor se componen de grupos de controles, menús, listas o colecciones de elementos y comandos.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="b2e7a-141">El marco de trabajo distingue entre dos tipos de contenedores, estáticos y dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="b2e7a-142">Contenedores estáticos</span><span class="sxs-lookup"><span data-stu-id="b2e7a-142">Static Containers</span></span>

<span data-ttu-id="b2e7a-143">Los contenedores estáticos se declaran y rellenan, junto con todos los recursos asociados, en el archivo de marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="b2e7a-144">Estos controles no se pueden modificar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="b2e7a-145">Entre las ventajas de los controles estáticos se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2e7a-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="b2e7a-146">Prototipos rápidos.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-146">Rapid prototyping.</span></span> <span data-ttu-id="b2e7a-147">Los controles estáticos permiten compilar rápidamente una maqueta de la cinta de opciones similar a un diseño final de la cinta de opciones que no requiere código complicado.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="b2e7a-148">Modificaciones sencillas.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-148">Easy modifications.</span></span> <span data-ttu-id="b2e7a-149">La mayoría de los elementos, los atributos, los recursos y los diseños de los controles estáticos se pueden modificar en el marcado.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="b2e7a-150">Interfaz de usuario coherente.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-150">Consistent UI.</span></span> <span data-ttu-id="b2e7a-151">Las aplicaciones bien diseñadas proporcionan una interfaz de usuario coherente y estable que evita los cambios en los menús y listas en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="b2e7a-152">En la tabla siguiente se describen los controles de contenedor estático en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="b2e7a-153">Control</span><span class="sxs-lookup"><span data-stu-id="b2e7a-153">Control</span></span>                                                        | <span data-ttu-id="b2e7a-154">Elemento de marcado</span><span class="sxs-lookup"><span data-stu-id="b2e7a-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b2e7a-155">Menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b2e7a-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="b2e7a-156">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="b2e7a-157">Cuadro emergente de contexto</span><span class="sxs-lookup"><span data-stu-id="b2e7a-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="b2e7a-158">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="b2e7a-159">Botón desplegable</span><span class="sxs-lookup"><span data-stu-id="b2e7a-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="b2e7a-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="b2e7a-161">Grupo</span><span class="sxs-lookup"><span data-stu-id="b2e7a-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="b2e7a-162">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="b2e7a-163">Grupo de menús</span><span class="sxs-lookup"><span data-stu-id="b2e7a-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="b2e7a-164">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="b2e7a-165">Botón de expansión</span><span class="sxs-lookup"><span data-stu-id="b2e7a-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="b2e7a-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="b2e7a-167">Tabulación</span><span class="sxs-lookup"><span data-stu-id="b2e7a-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="b2e7a-168">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="b2e7a-169">Grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="b2e7a-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="b2e7a-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="b2e7a-171">Contenedores dinámicos</span><span class="sxs-lookup"><span data-stu-id="b2e7a-171">Dynamic Containers</span></span>

<span data-ttu-id="b2e7a-172">Los contenedores dinámicos se declaran en el archivo de marcado de la cinta.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="b2e7a-173">Incluyen un grupo de elementos o comandos que se crean o modifican en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="b2e7a-174">Una subclase de contenedores dinámicos, denominados galerías, se distingue por su implementación de la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="b2e7a-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="b2e7a-175">Esta interfaz permite a un control exponer su elemento o lista de comandos como una colección, y admitir actualizaciones basadas en las condiciones de interacción con el usuario y en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="b2e7a-176">Para obtener más información, vea [trabajar con galerías](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="b2e7a-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="b2e7a-177">En la tabla siguiente se enumeran los controles de contenedor dinámico en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="b2e7a-178">Control</span><span class="sxs-lookup"><span data-stu-id="b2e7a-178">Control</span></span>                                                               | <span data-ttu-id="b2e7a-179">Elemento de marcado</span><span class="sxs-lookup"><span data-stu-id="b2e7a-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="b2e7a-180">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="b2e7a-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="b2e7a-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="b2e7a-182">Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="b2e7a-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="b2e7a-183">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="b2e7a-184">En la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b2e7a-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="b2e7a-185">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="b2e7a-186">Barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="b2e7a-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="b2e7a-187">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="b2e7a-188">Elementos recientes</span><span class="sxs-lookup"><span data-stu-id="b2e7a-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="b2e7a-189">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="b2e7a-190">Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="b2e7a-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="b2e7a-191">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="b2e7a-192">Controles especializados</span><span class="sxs-lookup"><span data-stu-id="b2e7a-192">Specialized Controls</span></span>

<span data-ttu-id="b2e7a-193">El marco de cinta de opciones contiene una serie de controles especializados para la funcionalidad específica de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="b2e7a-194">En la tabla siguiente se enumeran los controles especializados en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b2e7a-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="b2e7a-195">Control</span><span class="sxs-lookup"><span data-stu-id="b2e7a-195">Control</span></span>                                                                  | <span data-ttu-id="b2e7a-196">Elemento de marcado</span><span class="sxs-lookup"><span data-stu-id="b2e7a-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="b2e7a-197">Selector de colores desplegables</span><span class="sxs-lookup"><span data-stu-id="b2e7a-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="b2e7a-198">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="b2e7a-199">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="b2e7a-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="b2e7a-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="b2e7a-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="b2e7a-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e7a-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e7a-202">Descripción de los comandos y los controles</span><span class="sxs-lookup"><span data-stu-id="b2e7a-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 