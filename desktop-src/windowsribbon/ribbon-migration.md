---
title: Migrar al marco de cinta de Windows
description: Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario enriquecida, dinámica y controlada por contexto del sistema de comandos de la cinta de opciones de Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Cinta de Windows, migrar a
- Cinta de opciones, migrar a
- migrar a la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487959"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="e954f-106">Migrar al marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="e954f-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="e954f-107">Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario enriquecida, dinámica y controlada por contexto del sistema de comandos de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e954f-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="e954f-108">Esta es una manera fácil y eficaz de modernizar y revitalizar la aplicación, a la vez que mejora la accesibilidad, la facilidad de uso y la capacidad de detección de su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="e954f-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="e954f-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="e954f-109">Introduction</span></span>

<span data-ttu-id="e954f-110">En general, la migración de una aplicación existente al marco de la cinta de opciones implica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="e954f-111">Diseñar un diseño de cinta y controlar la organización que expone la funcionalidad de la aplicación existente y es lo suficientemente flexible como para admitir nuevas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="e954f-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="e954f-112">Adaptación del código de la aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="e954f-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="e954f-113">Migrar los recursos de la aplicación existentes (cadenas e imágenes) al marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="e954f-114">Las [instrucciones](https://msdn.microsoft.com/library/cc872782.aspx) para la experiencia del usuario de la cinta deben revisarse para determinar si la aplicación es una candidata adecuada para una interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="e954f-115">Diseñar el diseño de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="e954f-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="e954f-116">Se pueden identificar diseños de interfaz de usuario de cinta potenciales y diseños de control siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="e954f-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="e954f-117">Realizar el inventario de toda la funcionalidad existente.</span><span class="sxs-lookup"><span data-stu-id="e954f-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="e954f-118">Convertir esta funcionalidad en comandos de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="e954f-119">Organizar los comandos en grupos lógicos.</span><span class="sxs-lookup"><span data-stu-id="e954f-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="e954f-120">Realizar inventario</span><span class="sxs-lookup"><span data-stu-id="e954f-120">Take Inventory</span></span>

<span data-ttu-id="e954f-121">En el marco de la cinta de opciones, la funcionalidad expuesta por una aplicación que manipula el estado o la vista de un área de trabajo o documento se considera un comando.</span><span class="sxs-lookup"><span data-stu-id="e954f-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="e954f-122">Lo que constituye un comando puede variar y depende de la naturaleza y el dominio de la aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="e954f-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="e954f-123">En la tabla siguiente se muestra un conjunto de comandos básicos para una aplicación de edición de texto hipotética:</span><span class="sxs-lookup"><span data-stu-id="e954f-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="e954f-124">Símbolo</span><span class="sxs-lookup"><span data-stu-id="e954f-124">Symbol</span></span>           | <span data-ttu-id="e954f-125">id</span><span class="sxs-lookup"><span data-stu-id="e954f-125">ID</span></span>     | <span data-ttu-id="e954f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e954f-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="e954f-127">archivo de ID. \_ \_ nuevo</span><span class="sxs-lookup"><span data-stu-id="e954f-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="e954f-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="e954f-128">0xE100</span></span> | <span data-ttu-id="e954f-129">Nuevo documento</span><span class="sxs-lookup"><span data-stu-id="e954f-129">New document</span></span>              |
| <span data-ttu-id="e954f-130">archivo de identificador \_ \_ guardado</span><span class="sxs-lookup"><span data-stu-id="e954f-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="e954f-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="e954f-131">0xE103</span></span> | <span data-ttu-id="e954f-132">Guardar documento</span><span class="sxs-lookup"><span data-stu-id="e954f-132">Save document</span></span>             |
| <span data-ttu-id="e954f-133">archivo de ID. \_ \_ guardado</span><span class="sxs-lookup"><span data-stu-id="e954f-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="e954f-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="e954f-134">0xE104</span></span> | <span data-ttu-id="e954f-135">Guardar como... diálogo</span><span class="sxs-lookup"><span data-stu-id="e954f-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="e954f-136">IDENTIFICADOR de \_ archivo \_ abierto</span><span class="sxs-lookup"><span data-stu-id="e954f-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="e954f-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="e954f-137">0xE101</span></span> | <span data-ttu-id="e954f-138">Abrir... diálogo</span><span class="sxs-lookup"><span data-stu-id="e954f-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="e954f-139">\_salida de archivo de identificador \_</span><span class="sxs-lookup"><span data-stu-id="e954f-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="e954f-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="e954f-140">0xE102</span></span> | <span data-ttu-id="e954f-141">Salir de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e954f-141">Exit the application</span></span>      |
| <span data-ttu-id="e954f-142">deshacer edición de ID. \_ \_</span><span class="sxs-lookup"><span data-stu-id="e954f-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="e954f-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="e954f-143">0xE12B</span></span> | <span data-ttu-id="e954f-144">Deshacer</span><span class="sxs-lookup"><span data-stu-id="e954f-144">Undo</span></span>                      |
| <span data-ttu-id="e954f-145">\_cortar edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="e954f-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="e954f-146">0xE123</span></span> | <span data-ttu-id="e954f-147">Cortar el texto seleccionado</span><span class="sxs-lookup"><span data-stu-id="e954f-147">Cut selected text</span></span>         |
| <span data-ttu-id="e954f-148">\_editar la \_ copia de edición</span><span class="sxs-lookup"><span data-stu-id="e954f-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="e954f-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="e954f-149">0xE122</span></span> | <span data-ttu-id="e954f-150">Copiar texto seleccionado</span><span class="sxs-lookup"><span data-stu-id="e954f-150">Copy selected text</span></span>        |
| <span data-ttu-id="e954f-151">\_pegar edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="e954f-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="e954f-152">0xE125</span></span> | <span data-ttu-id="e954f-153">Pegar texto del portapapeles</span><span class="sxs-lookup"><span data-stu-id="e954f-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="e954f-154">\_borrado de edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="e954f-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="e954f-155">0xE120</span></span> | <span data-ttu-id="e954f-156">Eliminar texto seleccionado</span><span class="sxs-lookup"><span data-stu-id="e954f-156">Delete selected text</span></span>      |
| <span data-ttu-id="e954f-157">\_zoom de vista de identificador \_</span><span class="sxs-lookup"><span data-stu-id="e954f-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="e954f-158">1242</span><span class="sxs-lookup"><span data-stu-id="e954f-158">1242</span></span>   | <span data-ttu-id="e954f-159">Acercar... diálogo</span><span class="sxs-lookup"><span data-stu-id="e954f-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="e954f-160">Mire más allá de los menús y las barras de herramientas existentes al crear un inventario de comandos.</span><span class="sxs-lookup"><span data-stu-id="e954f-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="e954f-161">Tenga en cuenta todas las formas en que un usuario puede interactuar con el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e954f-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="e954f-162">Aunque no todos los comandos son adecuados para su inclusión en la cinta de opciones, este ejercicio puede exponer muy bien comandos ocultos previamente por capas de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e954f-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="e954f-163">Translate</span><span class="sxs-lookup"><span data-stu-id="e954f-163">Translate</span></span>

<span data-ttu-id="e954f-164">No todos los comandos deben representarse en la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="e954f-165">Por ejemplo, al escribir texto, cambiar una selección, desplazarse o mover el punto de inserción con el mouse todos los comandos se pueden incluir en el editor de texto hipotético, sin embargo, estos no son adecuados para exponer en una barra de comandos, ya que cada uno implica una interacción directa con la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e954f-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="e954f-166">Por el contrario, algunas funciones no se pueden considerar como un comando en el sentido tradicional.</span><span class="sxs-lookup"><span data-stu-id="e954f-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="e954f-167">Por ejemplo, en lugar de estar escondido en un cuadro de diálogo, los ajustes de los márgenes de la página de la impresora se pueden representar en la cinta de opciones como un grupo de controles de número en una pestaña o [modo de aplicación](ribbon-applicationmodes.md)contextual.</span><span class="sxs-lookup"><span data-stu-id="e954f-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="e954f-168">Anote el identificador numérico que se puede asignar a cada comando.</span><span class="sxs-lookup"><span data-stu-id="e954f-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="e954f-169">Algunos marcos de interfaz de usuario, como Microsoft Foundation Classes (MFC), definen identificadores para comandos como el menú Archivo y edición (0xE100 a 0xE200).</span><span class="sxs-lookup"><span data-stu-id="e954f-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="e954f-170">Organizar</span><span class="sxs-lookup"><span data-stu-id="e954f-170">Organize</span></span>

<span data-ttu-id="e954f-171">Antes de intentar organizar el inventario de comandos, se deben revisar las directrices de la [experiencia del usuario](https://msdn.microsoft.com/library/cc872782.aspx) en la cinta para obtener los procedimientos recomendados al implementar una interfaz de usuario de la cinta.</span><span class="sxs-lookup"><span data-stu-id="e954f-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="e954f-172">En general, se pueden aplicar las siguientes reglas a la organización de comandos de la cinta de opciones:</span><span class="sxs-lookup"><span data-stu-id="e954f-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="e954f-173">Es más probable que los comandos que operan en el archivo o en la aplicación global pertenezcan al menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="e954f-174">Los comandos usados con frecuencia, como cortar, copiar y pegar (como en el ejemplo del editor de texto), normalmente se colocan en una pestaña Inicio predeterminada. En aplicaciones más complejas, se pueden duplicar en otra parte de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="e954f-175">Los comandos importantes o usados con frecuencia podrían garantizar la inclusión predeterminada en la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="e954f-176">El marco de la cinta de opciones también proporciona controles ContextMenu y MiniToolbar a través de la vista ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="e954f-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="e954f-177">Estas características no son obligatorias, pero si la aplicación tiene uno o varios menús contextuales existentes, la migración de los comandos que contienen puede permitir la reutilización del código base existente con el enlace automático a los recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="e954f-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="e954f-178">Dado que cada aplicación es diferente, lea las instrucciones e intente aplicarlas a la máxima medida posible.</span><span class="sxs-lookup"><span data-stu-id="e954f-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="e954f-179">Uno de los objetivos del marco de la cinta de opciones es proporcionar una experiencia de usuario familiar y coherente, y este objetivo será más factible si los diseños de nuevas aplicaciones reflejan las aplicaciones de cinta existentes lo máximo posible.</span><span class="sxs-lookup"><span data-stu-id="e954f-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="e954f-180">Adaptación del código</span><span class="sxs-lookup"><span data-stu-id="e954f-180">Adapt Your Code</span></span>

<span data-ttu-id="e954f-181">Una vez que los comandos de la cinta de opciones se han identificado y organizado en agrupaciones lógicas, el número de pasos implicados al incorporar el marco de cinta en el código de aplicación existente depende de la complejidad de la aplicación original.</span><span class="sxs-lookup"><span data-stu-id="e954f-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="e954f-182">En general, hay tres pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="e954f-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="e954f-183">Cree el marcado de la cinta de opciones en función de la organización de comandos y la especificación de diseño.</span><span class="sxs-lookup"><span data-stu-id="e954f-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="e954f-184">Reemplazar la funcionalidad heredada de menús y barras de herramientas por la funcionalidad de la cinta.</span><span class="sxs-lookup"><span data-stu-id="e954f-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="e954f-185">Implemente un adaptador de IUICommandHandler.</span><span class="sxs-lookup"><span data-stu-id="e954f-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="e954f-186">Crear el marcado</span><span class="sxs-lookup"><span data-stu-id="e954f-186">Create The Markup</span></span>

<span data-ttu-id="e954f-187">La lista de comandos, así como su organización y diseño, se declaran a través del archivo de marcado de la cinta de opciones utilizado por el [compilador de marcado](windowsribbon-intentcl.md)de la cinta.</span><span class="sxs-lookup"><span data-stu-id="e954f-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="e954f-188">Muchos de los pasos necesarios para adaptar una aplicación existente son similares a los necesarios para iniciar una nueva aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="e954f-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="e954f-189">Para obtener más información, consulte el tutorial [creación de una aplicación de cinta](windowsribbon-stepbystep.md) para obtener una nueva aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="e954f-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="e954f-190">Hay dos secciones principales en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="e954f-191">La primera sección es un manifiesto de comandos y sus recursos asociados (cadenas e imágenes).</span><span class="sxs-lookup"><span data-stu-id="e954f-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="e954f-192">La segunda sección especifica la estructura y la ubicación de los controles en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="e954f-193">El marcado para el editor de texto simple podría ser similar al del ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="e954f-194">Los recursos de imagen y de cadena se describen más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="e954f-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="e954f-195">Para evitar la redefinición de símbolos definidos por un marco de interfaz de usuario como MFC, en el ejemplo anterior se usan nombres de símbolos ligeramente diferentes para cada comando (archivo de ID. \_ \_ nuevo frente a ID \_ cmd \_ nuevo).</span><span class="sxs-lookup"><span data-stu-id="e954f-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="e954f-196">Sin embargo, el identificador numérico asignado a cada comando debe ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="e954f-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="e954f-197">Para integrar el archivo de marcado en una aplicación, configure un paso de compilación personalizada para ejecutar el compilador de marcado de la cinta de opciones UICC.exe.</span><span class="sxs-lookup"><span data-stu-id="e954f-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="e954f-198">El encabezado y los archivos de recursos resultantes se incorporan en el proyecto existente.</span><span class="sxs-lookup"><span data-stu-id="e954f-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="e954f-199">Si la aplicación de la cinta de opciones editor de texto de ejemplo se denomina "RibbonPad", se requiere una línea de comandos de compilación personalizada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="e954f-200">El compilador de marcado crea un archivo binario, un archivo de encabezado (H) y un archivo de recursos (RC).</span><span class="sxs-lookup"><span data-stu-id="e954f-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="e954f-201">Dado que es probable que la aplicación existente tenga un archivo RC existente, incluya los archivos H y RC generados en ese archivo RC, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="e954f-202">Reemplazar barras de herramientas y menús heredados</span><span class="sxs-lookup"><span data-stu-id="e954f-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="e954f-203">Reemplazar los menús y las barras de herramientas estándar con una cinta de opciones en una aplicación heredada requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="e954f-204">Quite las referencias de recursos de menús y barras de herramientas del archivo de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e954f-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="e954f-205">Elimine todo el código de inicialización de la barra de herramientas y del menú.</span><span class="sxs-lookup"><span data-stu-id="e954f-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="e954f-206">Elimine cualquier código utilizado para adjuntar una barra de herramientas o una barra de menús a la ventana de nivel superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e954f-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="e954f-207">Cree una instancia del marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="e954f-208">Adjunte la cinta de opciones a la ventana de nivel superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e954f-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="e954f-209">Cargar el marcado compilado.</span><span class="sxs-lookup"><span data-stu-id="e954f-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e954f-210">La barra de estado y las tablas de métodos abreviados de teclado existentes deben conservarse, ya que el marco de cinta no reemplaza estas características.</span><span class="sxs-lookup"><span data-stu-id="e954f-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="e954f-211">En el ejemplo siguiente se muestra cómo inicializar el marco de trabajo mediante [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span><span class="sxs-lookup"><span data-stu-id="e954f-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="e954f-212">En el ejemplo siguiente se muestra cómo usar [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para cargar el marcado compilado:</span><span class="sxs-lookup"><span data-stu-id="e954f-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="e954f-213">La clase CApplication, a la que se hace referencia anteriormente, debe implementar un par de interfaces del modelo de objetos componentes (COM) definidas por el marco de la cinta de opciones: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) y [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="e954f-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="e954f-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) proporciona la interfaz de devolución de llamada principal entre el marco de trabajo y la aplicación (por ejemplo, el alto de la cinta de opciones se comunica a través de [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) mientras que las devoluciones de llamada para comandos individuales se proporcionan en respuesta a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span><span class="sxs-lookup"><span data-stu-id="e954f-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="e954f-215">**Sugerencia:** Algunos marcos de trabajo de la aplicación, como MFC, requieren que se tenga en cuenta el alto de la barra de cinta al representar el espacio de documento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e954f-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="e954f-216">En estos casos, es necesario agregar una ventana oculta para superponer la barra de cinta y forzar el espacio del documento al alto deseado.</span><span class="sxs-lookup"><span data-stu-id="e954f-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="e954f-217">Para obtener un ejemplo de este enfoque, en el que se llama a una función de diseño basada en el alto de la cinta de opciones devuelto por el método [**IUIRibbon:: getHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , vea el [ejemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="e954f-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="e954f-218">En el ejemplo de código siguiente se muestra una implementación de [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :</span><span class="sxs-lookup"><span data-stu-id="e954f-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="e954f-219">Implementar un adaptador de IUICommandHandler</span><span class="sxs-lookup"><span data-stu-id="e954f-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="e954f-220">Dependiendo del diseño de la aplicación original, es posible que sea más fácil tener varias implementaciones de controlador de comandos o un solo controlador de comandos de puente que invoque la lógica de comandos de la aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="e954f-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="e954f-221">Muchas aplicaciones usan \_ mensajes de comandos de WM para este propósito en los que es suficiente proporcionar un controlador de comandos único y para todos los propósitos que simplemente reenvía \_ los mensajes de comandos de WM a la ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e954f-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="e954f-222">Sin embargo, este enfoque requiere un tratamiento especial para comandos como **Exit** o **Close**.</span><span class="sxs-lookup"><span data-stu-id="e954f-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="e954f-223">Dado que la cinta de opciones no se puede destruir mientras está procesando un mensaje de ventana, el \_ mensaje de cierre de WM debe publicarse en el subproceso de la interfaz de usuario de la aplicación y no debe procesarse sincrónicamente, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e954f-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="e954f-224">Migrar recursos</span><span class="sxs-lookup"><span data-stu-id="e954f-224">Migrating Resources</span></span>

<span data-ttu-id="e954f-225">Una vez que se ha definido el manifiesto de comandos, se ha declarado la estructura de la cinta de opciones y el código de aplicación se ha adaptado para hospedar el marco de cinta, el último paso es la especificación de los recursos de cadena e imagen para cada comando.</span><span class="sxs-lookup"><span data-stu-id="e954f-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="e954f-226">Los recursos de cadena e imagen se proporcionan normalmente en el archivo de marcado.</span><span class="sxs-lookup"><span data-stu-id="e954f-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="e954f-227">Sin embargo, se pueden generar o reemplazar mediante programación implementando el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="e954f-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="e954f-228">Recursos de cadena</span><span class="sxs-lookup"><span data-stu-id="e954f-228">String Resources</span></span>

<span data-ttu-id="e954f-229">[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) es la propiedad de cadena más común definida para un comando.</span><span class="sxs-lookup"><span data-stu-id="e954f-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="e954f-230">Se representan como etiquetas de texto para pestañas, grupos y controles individuales.</span><span class="sxs-lookup"><span data-stu-id="e954f-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="e954f-231">Normalmente, una cadena de etiqueta de un elemento de menú heredado se puede volver a usar para un **comando. LabelTitle** sin mucha edición.</span><span class="sxs-lookup"><span data-stu-id="e954f-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="e954f-232">Sin embargo, las siguientes convenciones han cambiado con la llegada de la cinta de opciones:</span><span class="sxs-lookup"><span data-stu-id="e954f-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="e954f-233">El sufijo de puntos suspensivos (...), que se usa para indicar un comando de inicio de diálogo, ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="e954f-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="e954f-234">El símbolo de y comercial (&) se puede seguir usando para indicar un método abreviado de teclado para un comando que aparece en un menú, pero la propiedad [**Command. KeyTip**](windowsribbon-element-command-keytip.md) compatible con el marco de trabajo cumple un propósito similar.</span><span class="sxs-lookup"><span data-stu-id="e954f-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="e954f-235">En el ejemplo de editor de texto, se pueden especificar las siguientes cadenas para LabelTitle y KeyTip:</span><span class="sxs-lookup"><span data-stu-id="e954f-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="e954f-236">Símbolo</span><span class="sxs-lookup"><span data-stu-id="e954f-236">Symbol</span></span>           | <span data-ttu-id="e954f-237">Cadena original</span><span class="sxs-lookup"><span data-stu-id="e954f-237">Original string</span></span> | <span data-ttu-id="e954f-238">Cadena LabelTitle</span><span class="sxs-lookup"><span data-stu-id="e954f-238">LabelTitle string</span></span> | <span data-ttu-id="e954f-239">Cadena de KeyTip</span><span class="sxs-lookup"><span data-stu-id="e954f-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="e954f-240">archivo de ID. \_ \_ nuevo</span><span class="sxs-lookup"><span data-stu-id="e954f-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="e954f-241">&nuevo</span><span class="sxs-lookup"><span data-stu-id="e954f-241">&New</span></span>            | <span data-ttu-id="e954f-242">&nuevo</span><span class="sxs-lookup"><span data-stu-id="e954f-242">&New</span></span>              | <span data-ttu-id="e954f-243">N</span><span class="sxs-lookup"><span data-stu-id="e954f-243">N</span></span>             |
| <span data-ttu-id="e954f-244">archivo de identificador \_ \_ guardado</span><span class="sxs-lookup"><span data-stu-id="e954f-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="e954f-245">&guardar</span><span class="sxs-lookup"><span data-stu-id="e954f-245">&Save</span></span>           | <span data-ttu-id="e954f-246">&guardar</span><span class="sxs-lookup"><span data-stu-id="e954f-246">&Save</span></span>             | <span data-ttu-id="e954f-247">S</span><span class="sxs-lookup"><span data-stu-id="e954f-247">S</span></span>             |
| <span data-ttu-id="e954f-248">archivo de ID. \_ \_ guardado</span><span class="sxs-lookup"><span data-stu-id="e954f-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="e954f-249">Guardar &como...</span><span class="sxs-lookup"><span data-stu-id="e954f-249">Save &As…</span></span>       | <span data-ttu-id="e954f-250">Guardar &como</span><span class="sxs-lookup"><span data-stu-id="e954f-250">Save &as</span></span>          | <span data-ttu-id="e954f-251">A</span><span class="sxs-lookup"><span data-stu-id="e954f-251">A</span></span>             |
| <span data-ttu-id="e954f-252">IDENTIFICADOR de \_ archivo \_ abierto</span><span class="sxs-lookup"><span data-stu-id="e954f-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="e954f-253">&abrir...</span><span class="sxs-lookup"><span data-stu-id="e954f-253">&Open…</span></span>          | <span data-ttu-id="e954f-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="e954f-254">&Open</span></span>             | <span data-ttu-id="e954f-255">O</span><span class="sxs-lookup"><span data-stu-id="e954f-255">O</span></span>             |
| <span data-ttu-id="e954f-256">\_salida de archivo de identificador \_</span><span class="sxs-lookup"><span data-stu-id="e954f-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="e954f-257">&Salir</span><span class="sxs-lookup"><span data-stu-id="e954f-257">E&xit</span></span>           | <span data-ttu-id="e954f-258">&Salir</span><span class="sxs-lookup"><span data-stu-id="e954f-258">E&xit</span></span>             | <span data-ttu-id="e954f-259">X</span><span class="sxs-lookup"><span data-stu-id="e954f-259">X</span></span>             |
| <span data-ttu-id="e954f-260">deshacer edición de ID. \_ \_</span><span class="sxs-lookup"><span data-stu-id="e954f-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="e954f-261">Deshacer &</span><span class="sxs-lookup"><span data-stu-id="e954f-261">&Undo</span></span>           | <span data-ttu-id="e954f-262">Deshacer</span><span class="sxs-lookup"><span data-stu-id="e954f-262">Undo</span></span>              | <span data-ttu-id="e954f-263">Z</span><span class="sxs-lookup"><span data-stu-id="e954f-263">Z</span></span>             |
| <span data-ttu-id="e954f-264">\_cortar edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="e954f-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="e954f-265">Cu&t</span></span>            | <span data-ttu-id="e954f-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="e954f-266">Cu&t</span></span>              | <span data-ttu-id="e954f-267">X</span><span class="sxs-lookup"><span data-stu-id="e954f-267">X</span></span>             |
| <span data-ttu-id="e954f-268">\_editar la \_ copia de edición</span><span class="sxs-lookup"><span data-stu-id="e954f-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="e954f-269">&copiar</span><span class="sxs-lookup"><span data-stu-id="e954f-269">&Copy</span></span>           | <span data-ttu-id="e954f-270">&copiar</span><span class="sxs-lookup"><span data-stu-id="e954f-270">&Copy</span></span>             | <span data-ttu-id="e954f-271">C</span><span class="sxs-lookup"><span data-stu-id="e954f-271">C</span></span>             |
| <span data-ttu-id="e954f-272">\_pegar edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="e954f-273">&pegar</span><span class="sxs-lookup"><span data-stu-id="e954f-273">&Paste</span></span>          | <span data-ttu-id="e954f-274">&pegar</span><span class="sxs-lookup"><span data-stu-id="e954f-274">&Paste</span></span>            | <span data-ttu-id="e954f-275">V</span><span class="sxs-lookup"><span data-stu-id="e954f-275">V</span></span>             |
| <span data-ttu-id="e954f-276">\_borrado de edición de ID. \_</span><span class="sxs-lookup"><span data-stu-id="e954f-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="e954f-277">&eliminar</span><span class="sxs-lookup"><span data-stu-id="e954f-277">&Delete</span></span>         | <span data-ttu-id="e954f-278">&eliminar</span><span class="sxs-lookup"><span data-stu-id="e954f-278">&Delete</span></span>           | <span data-ttu-id="e954f-279">D</span><span class="sxs-lookup"><span data-stu-id="e954f-279">D</span></span>             |
| <span data-ttu-id="e954f-280">\_zoom de vista de identificador \_</span><span class="sxs-lookup"><span data-stu-id="e954f-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="e954f-281">&zoom...</span><span class="sxs-lookup"><span data-stu-id="e954f-281">&Zoom…</span></span>          | <span data-ttu-id="e954f-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="e954f-282">Zoom</span></span>              | <span data-ttu-id="e954f-283">Z</span><span class="sxs-lookup"><span data-stu-id="e954f-283">Z</span></span>             |



 

<span data-ttu-id="e954f-284">A continuación se muestra una lista de otras propiedades de cadena que se deben establecer en la mayoría de los comandos:</span><span class="sxs-lookup"><span data-stu-id="e954f-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="e954f-285">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="e954f-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="e954f-286">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="e954f-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="e954f-287">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="e954f-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="e954f-288">Ahora se pueden declarar pestañas, grupos y otras características de la interfaz de usuario de la cinta de opciones con todos los recursos de cadena e imagen especificados.</span><span class="sxs-lookup"><span data-stu-id="e954f-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="e954f-289">En el siguiente ejemplo de marcado de cinta se muestran varios recursos de cadena:</span><span class="sxs-lookup"><span data-stu-id="e954f-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="e954f-290">Recursos de imagen</span><span class="sxs-lookup"><span data-stu-id="e954f-290">Image Resources</span></span>

<span data-ttu-id="e954f-291">El marco de cinta admite formatos de imagen que proporcionan una apariencia mucho más enriquecida que los formatos de imagen admitidos por los componentes de menú y barra de herramientas anteriores.</span><span class="sxs-lookup"><span data-stu-id="e954f-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="e954f-292">En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.</span><span class="sxs-lookup"><span data-stu-id="e954f-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="e954f-293">En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.</span><span class="sxs-lookup"><span data-stu-id="e954f-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="e954f-294">Los archivos de imagen existentes se pueden convertir a cualquier formato.</span><span class="sxs-lookup"><span data-stu-id="e954f-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="e954f-295">Sin embargo, los resultados pueden ser menos satisfactorios si los archivos de imagen no admiten el suavizado de contorno y la transparencia.</span><span class="sxs-lookup"><span data-stu-id="e954f-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="e954f-296">No es posible especificar un tamaño predeterminado único para los recursos de imagen en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e954f-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="e954f-297">Sin embargo, para admitir el [diseño adaptable](windowsribbon-templates.md) de los controles, las imágenes se pueden especificar en dos tamaños (grande y pequeño).</span><span class="sxs-lookup"><span data-stu-id="e954f-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="e954f-298">Todas las imágenes en el marco de cinta se escalan según la resolución de puntos por pulgada (PPP) de la pantalla con el tamaño representado exacto que depende de esta configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="e954f-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="e954f-299">Consulte [especificar recursos de imagen de cinta](windowsribbon-imageformats.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e954f-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="e954f-300">En el ejemplo siguiente se muestra cómo se hace referencia a un conjunto de imágenes específicas de PPP en el marcado:</span><span class="sxs-lookup"><span data-stu-id="e954f-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="e954f-301">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e954f-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e954f-302">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="e954f-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 