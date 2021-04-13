---
description: Un objeto de controlador de extensión de Shell debe registrarse antes de que el shell pueda usarlo. Este tema es una discusión general sobre cómo registrar un controlador de extensión de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrando controladores de extensión de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985762"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="f3aec-104">Registrando controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="f3aec-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="f3aec-105">Un objeto de controlador de extensión de Shell debe registrarse antes de que el shell pueda usarlo.</span><span class="sxs-lookup"><span data-stu-id="f3aec-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="f3aec-106">Este tema es una discusión general sobre cómo registrar un controlador de extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="f3aec-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="f3aec-107">Cada vez que crea o cambia un controlador de extensión de Shell, es importante notificar al sistema que ha realizado un cambio.</span><span class="sxs-lookup"><span data-stu-id="f3aec-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="f3aec-108">Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el evento **\_ ASSOCCHANGED de SHCNE** .</span><span class="sxs-lookup"><span data-stu-id="f3aec-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="f3aec-109">Si no llama a **SHChangeNotify**, es posible que no se reconozca el cambio hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="f3aec-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="f3aec-110">Hay algunos factores adicionales que se aplican a los sistemas 2000 de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3aec-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="f3aec-111">Para obtener más información, consulte la sección [registro de controladores de extensión de Shell en Windows 2000 Systems](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="f3aec-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="f3aec-112">Al igual que con todos los objetos del modelo de objetos componentes (COM), debe crear un GUID para el controlador mediante una herramienta como Guidgen.exe, que se proporciona con el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3aec-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3aec-113">Cree una subclave en **HKEY \_ classes \_ raíz** \\ **CLSID** cuyo nombre es la forma de cadena de ese GUID.</span><span class="sxs-lookup"><span data-stu-id="f3aec-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="f3aec-114">Dado que los controladores de la extensión de Shell son servidores en proceso, también debe crear una subclave **InProcServer32** en esa subclave GUID con el valor (predeterminado) establecido en la ruta de acceso de la dll del controlador.</span><span class="sxs-lookup"><span data-stu-id="f3aec-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="f3aec-115">Use el modelo de subprocesos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="f3aec-115">Use the apartment threading model.</span></span> <span data-ttu-id="f3aec-116">A continuación, se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3aec-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="f3aec-117">Cada vez que el shell realiza una acción que puede incluir un controlador de extensión de Shell, comprueba la subclave del registro adecuada.</span><span class="sxs-lookup"><span data-stu-id="f3aec-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="f3aec-118">La subclave bajo la que un controlador de extensión registra los controles cuando se llama.</span><span class="sxs-lookup"><span data-stu-id="f3aec-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="f3aec-119">Por ejemplo, es una práctica común tener un controlador de menú contextual llamado cuando el shell muestra un menú contextual para un miembro de un [tipo de archivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f3aec-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="f3aec-120">En este caso, el controlador se debe registrar en la subclave **ProgID** del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f3aec-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="f3aec-121">En este tema se tratan los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="f3aec-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="f3aec-122">Nombres de controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="f3aec-123">Objetos de Shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="f3aec-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="f3aec-124">Ejemplo de registro de un controlador de extensión</span><span class="sxs-lookup"><span data-stu-id="f3aec-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="f3aec-125">Registrando controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="f3aec-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="f3aec-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3aec-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="f3aec-127">Nombres de controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-127">Handler Names</span></span>

<span data-ttu-id="f3aec-128">Para habilitar un controlador de extensión de Shell, cree una subclave con el nombre de la subclave del controlador (consulte a continuación) en la subclave **ShellEx** del **ProgID** (para tipos de archivo) o el nombre del tipo de objeto de Shell (para [ \_ \_ objetos de Shell predefinidos](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="f3aec-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="f3aec-129">Por ejemplo, si desea registrar un controlador de extensión de menú contextual para el programa. 1, empiece por crear la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="f3aec-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="f3aec-130">En el caso de los siguientes controladores, cree una subclave debajo de la subclave "Handlet subclave name" denominada como la versión de cadena del identificador de clase (CLSID) de la extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="f3aec-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="f3aec-131">Se pueden registrar varias extensiones en el nombre de la subclave del controlador mediante la creación de varias subclaves.</span><span class="sxs-lookup"><span data-stu-id="f3aec-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="f3aec-132">Controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-132">Handler</span></span>                 | <span data-ttu-id="f3aec-133">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f3aec-133">Interface</span></span>          | <span data-ttu-id="f3aec-134">Nombre de la subclave del controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="f3aec-135">Controlador de proveedor de columnas</span><span class="sxs-lookup"><span data-stu-id="f3aec-135">Column provider handler</span></span> | <span data-ttu-id="f3aec-136">IColumnProvider</span><span class="sxs-lookup"><span data-stu-id="f3aec-136">IColumnProvider</span></span>    | <span data-ttu-id="f3aec-137">**ColumnHandlers**</span><span class="sxs-lookup"><span data-stu-id="f3aec-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="f3aec-138">Controlador del menú contextual</span><span class="sxs-lookup"><span data-stu-id="f3aec-138">Shortcut menu handler</span></span>   | <span data-ttu-id="f3aec-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="f3aec-139">IContextMenu</span></span>       | <span data-ttu-id="f3aec-140">**ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="f3aec-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="f3aec-141">Controlador Copyhook</span><span class="sxs-lookup"><span data-stu-id="f3aec-141">Copyhook handler</span></span>        | <span data-ttu-id="f3aec-142">ICopyHook</span><span class="sxs-lookup"><span data-stu-id="f3aec-142">ICopyHook</span></span>          | <span data-ttu-id="f3aec-143">**CopyHookHandlers**</span><span class="sxs-lookup"><span data-stu-id="f3aec-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="f3aec-144">Controlador de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="f3aec-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="f3aec-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="f3aec-145">IContextMenu</span></span>       | <span data-ttu-id="f3aec-146">**DragDropHandlers**</span><span class="sxs-lookup"><span data-stu-id="f3aec-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="f3aec-147">Controlador de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="f3aec-147">Property sheet handler</span></span>  | <span data-ttu-id="f3aec-148">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="f3aec-148">IShellPropSheetExt</span></span> | <span data-ttu-id="f3aec-149">**PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="f3aec-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="f3aec-150">En el caso de los siguientes controladores, el valor predeterminado de la clave "nombre de subclave de controlador" es la versión de cadena del CLSID de la extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="f3aec-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="f3aec-151">Solo se puede registrar una extensión para estos controladores.</span><span class="sxs-lookup"><span data-stu-id="f3aec-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="f3aec-152">Controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-152">Handler</span></span>                 | <span data-ttu-id="f3aec-153">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f3aec-153">Interface</span></span>            | <span data-ttu-id="f3aec-154">Nombre de la subclave del controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="f3aec-155">Controlador de datos</span><span class="sxs-lookup"><span data-stu-id="f3aec-155">Data handler</span></span>            | <span data-ttu-id="f3aec-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="f3aec-156">IDataObject</span></span>          | <span data-ttu-id="f3aec-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="f3aec-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="f3aec-158">Quitar controlador</span><span class="sxs-lookup"><span data-stu-id="f3aec-158">Drop handler</span></span>            | <span data-ttu-id="f3aec-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="f3aec-159">IDropTarget</span></span>          | <span data-ttu-id="f3aec-160">**DropHandler**</span><span class="sxs-lookup"><span data-stu-id="f3aec-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="f3aec-161">Controlador de iconos</span><span class="sxs-lookup"><span data-stu-id="f3aec-161">Icon handler</span></span>            | <span data-ttu-id="f3aec-162">IExtractIconA/W</span><span class="sxs-lookup"><span data-stu-id="f3aec-162">IExtractIconA/W</span></span>      | <span data-ttu-id="f3aec-163">**IconHandler**</span><span class="sxs-lookup"><span data-stu-id="f3aec-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="f3aec-164">Controlador de imagen en miniatura</span><span class="sxs-lookup"><span data-stu-id="f3aec-164">Thumbnail image handler</span></span> | <span data-ttu-id="f3aec-165">IThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="f3aec-165">IThumbnailProvider</span></span>   | <span data-ttu-id="f3aec-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="f3aec-167">Controlador de recuadro informativo</span><span class="sxs-lookup"><span data-stu-id="f3aec-167">Infotip handler</span></span>         | <span data-ttu-id="f3aec-168">IQueryInfo</span><span class="sxs-lookup"><span data-stu-id="f3aec-168">IQueryInfo</span></span>           | <span data-ttu-id="f3aec-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="f3aec-170">Vínculo de Shell (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3aec-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="f3aec-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="f3aec-171">IShellLinkA</span></span>          | <span data-ttu-id="f3aec-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="f3aec-173">Vínculo de Shell (Unicode)</span><span class="sxs-lookup"><span data-stu-id="f3aec-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="f3aec-174">IShellLinkW</span><span class="sxs-lookup"><span data-stu-id="f3aec-174">IShellLinkW</span></span>          | <span data-ttu-id="f3aec-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="f3aec-176">Almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="f3aec-176">Structured storage</span></span>      | <span data-ttu-id="f3aec-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="f3aec-177">IStorage</span></span>             | <span data-ttu-id="f3aec-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="f3aec-179">Metadatos</span><span class="sxs-lookup"><span data-stu-id="f3aec-179">Metadata</span></span>                | <span data-ttu-id="f3aec-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="f3aec-180">IPropertySetStorage</span></span>  | <span data-ttu-id="f3aec-181">**PropertyHandler**</span><span class="sxs-lookup"><span data-stu-id="f3aec-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="f3aec-182">Anclar al menú Inicio</span><span class="sxs-lookup"><span data-stu-id="f3aec-182">Pin to Start Menu</span></span>       | <span data-ttu-id="f3aec-183">IStartMenuPinnedList</span><span class="sxs-lookup"><span data-stu-id="f3aec-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="f3aec-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="f3aec-185">Anclar a la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="f3aec-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="f3aec-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="f3aec-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="f3aec-187">Las subclaves especificadas para agregar **anclar al menú Inicio** y **anclar a la barra de tareas** al menú contextual de un elemento solo son necesarias para los tipos de archivo que incluyen la entrada [IsShortCut](./links.md) .</span><span class="sxs-lookup"><span data-stu-id="f3aec-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="f3aec-188">Objetos de Shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="f3aec-188">Predefined Shell Objects</span></span>

<span data-ttu-id="f3aec-189">El shell define objetos adicionales en **la \_ \_ raíz de las clases HKEY** que se pueden extender de la misma manera que los tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f3aec-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="f3aec-190">Por ejemplo, para agregar un controlador de hoja de propiedades para todos los archivos, puede registrarse en la subclave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="f3aec-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="f3aec-191">En la tabla siguiente se proporcionan las diversas subclaves de **\_ las clases HKEY \_ raíz** en las que se pueden registrar controladores de extensión.</span><span class="sxs-lookup"><span data-stu-id="f3aec-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="f3aec-192">Tenga en cuenta que muchos controladores de extensión no se pueden registrar en todas las subclaves de la lista.</span><span class="sxs-lookup"><span data-stu-id="f3aec-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="f3aec-193">Para obtener más información, vea la documentación del controlador específico.</span><span class="sxs-lookup"><span data-stu-id="f3aec-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="f3aec-194">Subclave</span><span class="sxs-lookup"><span data-stu-id="f3aec-194">Subkey</span></span>                    | <span data-ttu-id="f3aec-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3aec-195">Description</span></span>                                                          | <span data-ttu-id="f3aec-196">Controladores posibles</span><span class="sxs-lookup"><span data-stu-id="f3aec-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="f3aec-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="f3aec-197">\**\** _</span></span>                    | <span data-ttu-id="f3aec-198">Todos los archivos</span><span class="sxs-lookup"><span data-stu-id="f3aec-198">All files</span></span>                                                            | <span data-ttu-id="f3aec-199">Menú contextual, hoja de propiedades, verbos (ver más abajo)</span><span class="sxs-lookup"><span data-stu-id="f3aec-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="f3aec-200">_ *AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="f3aec-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="f3aec-201">Todos los archivos y carpetas de archivos</span><span class="sxs-lookup"><span data-stu-id="f3aec-201">All files and file folders</span></span>                                           | <span data-ttu-id="f3aec-202">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-203">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="f3aec-203">**Folder**</span></span>                | <span data-ttu-id="f3aec-204">Todas las carpetas</span><span class="sxs-lookup"><span data-stu-id="f3aec-204">All folders</span></span>                                                          | <span data-ttu-id="f3aec-205">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-206">**Directorio**</span><span class="sxs-lookup"><span data-stu-id="f3aec-206">**Directory**</span></span>             | <span data-ttu-id="f3aec-207">Carpetas de archivos</span><span class="sxs-lookup"><span data-stu-id="f3aec-207">File folders</span></span>                                                         | <span data-ttu-id="f3aec-208">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-209">**Fondo de directorio \\**</span><span class="sxs-lookup"><span data-stu-id="f3aec-209">**Directory\\Background**</span></span> | <span data-ttu-id="f3aec-210">Fondo de carpeta de archivos</span><span class="sxs-lookup"><span data-stu-id="f3aec-210">File folder background</span></span>                                               | <span data-ttu-id="f3aec-211">Solo el menú contextual</span><span class="sxs-lookup"><span data-stu-id="f3aec-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="f3aec-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="f3aec-212">**DesktopBackground**</span></span>     | <span data-ttu-id="f3aec-213">Fondo de escritorio (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="f3aec-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="f3aec-214">Menú contextual, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="f3aec-215">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="f3aec-215">**Drive**</span></span>                 | <span data-ttu-id="f3aec-216">Todas las unidades de mi PC, como "C: \\ "</span><span class="sxs-lookup"><span data-stu-id="f3aec-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="f3aec-217">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-218">**Network**</span><span class="sxs-lookup"><span data-stu-id="f3aec-218">**Network**</span></span>               | <span data-ttu-id="f3aec-219">Red completa (en mis sitios de red)</span><span class="sxs-lookup"><span data-stu-id="f3aec-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="f3aec-220">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-221">**Tipo de red \\\\\#**</span><span class="sxs-lookup"><span data-stu-id="f3aec-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="f3aec-222">Todos los objetos de tipo \# (ver más abajo)</span><span class="sxs-lookup"><span data-stu-id="f3aec-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="f3aec-223">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="f3aec-224">**NetShare**</span></span>              | <span data-ttu-id="f3aec-225">Todos los recursos compartidos de red</span><span class="sxs-lookup"><span data-stu-id="f3aec-225">All network shares</span></span>                                                   | <span data-ttu-id="f3aec-226">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-227">**NetServer**</span><span class="sxs-lookup"><span data-stu-id="f3aec-227">**NetServer**</span></span>             | <span data-ttu-id="f3aec-228">Todos los servidores de red</span><span class="sxs-lookup"><span data-stu-id="f3aec-228">All network servers</span></span>                                                  | <span data-ttu-id="f3aec-229">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-230">*\_nombre del proveedor de red \_*</span><span class="sxs-lookup"><span data-stu-id="f3aec-230">*network\_provider\_name*</span></span> | <span data-ttu-id="f3aec-231">Todos los objetos proporcionados por el proveedor de red "*\_ \_ nombre de proveedor de red*"</span><span class="sxs-lookup"><span data-stu-id="f3aec-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="f3aec-232">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="f3aec-233">**Impresoras**</span><span class="sxs-lookup"><span data-stu-id="f3aec-233">**Printers**</span></span>              | <span data-ttu-id="f3aec-234">Todas las impresoras</span><span class="sxs-lookup"><span data-stu-id="f3aec-234">All printers</span></span>                                                         | <span data-ttu-id="f3aec-235">Menú contextual, hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="f3aec-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="f3aec-236">**Audio**</span><span class="sxs-lookup"><span data-stu-id="f3aec-236">**AudioCD**</span></span>               | <span data-ttu-id="f3aec-237">CD de audio en la unidad de CD</span><span class="sxs-lookup"><span data-stu-id="f3aec-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="f3aec-238">Solo verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-238">Verbs only</span></span>                                       |
| <span data-ttu-id="f3aec-239">**DISCOS**</span><span class="sxs-lookup"><span data-stu-id="f3aec-239">**DVD**</span></span>                   | <span data-ttu-id="f3aec-240">Unidad de DVD (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="f3aec-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="f3aec-241">Menú contextual, hoja de propiedades, verbos</span><span class="sxs-lookup"><span data-stu-id="f3aec-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="f3aec-242">Notas</span><span class="sxs-lookup"><span data-stu-id="f3aec-242">Notes</span></span>

-   <span data-ttu-id="f3aec-243">Para acceder al menú contextual de fondo de la carpeta de archivos, haga clic con el botón secundario en una carpeta de archivos, pero no en el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f3aec-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="f3aec-244">Los "verbos" son comandos especiales registrados en el verbo de Shell de la subclave **\_ \_ raíz de las clases HKEY** \\  \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="f3aec-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="f3aec-245">Para el tipo de **red** \\  \\ **\#** , " \# " es un código de tipo de proveedor de red en formato decimal.</span><span class="sxs-lookup"><span data-stu-id="f3aec-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="f3aec-246">El código de tipo de proveedor de red es la palabra alta de un tipo de red.</span><span class="sxs-lookup"><span data-stu-id="f3aec-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="f3aec-247">La lista de tipos de red se proporciona en el archivo de encabezado Winnetwk. h ( \_ valores de net WNNC \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="f3aec-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="f3aec-248">Por ejemplo, WNNC \_ net \_ Shiva es 0x00330000, por lo que la subclave de tipo correspondiente sería **HKEY \_ classes \_ root** \\ **Network** \\ **Type** \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="f3aec-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="f3aec-249">"*\_ \_ nombre de proveedor de red*" es un nombre de proveedor de red tal y como lo especifica [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con los espacios convertidos en guiones bajos.</span><span class="sxs-lookup"><span data-stu-id="f3aec-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="f3aec-250">Por ejemplo, si se instala el proveedor de red de redes de Microsoft, su nombre de proveedor es "red de Microsoft Windows" y el *\_ \_ nombre de proveedor de red* correspondiente es **\_ \_ red de Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="f3aec-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="f3aec-251">Ejemplo de registro de un controlador de extensión</span><span class="sxs-lookup"><span data-stu-id="f3aec-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="f3aec-252">Para habilitar un controlador determinado, cree una subclave en la subclave de tipo de controlador de extensión con el nombre del controlador.</span><span class="sxs-lookup"><span data-stu-id="f3aec-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="f3aec-253">El shell no utiliza el nombre del controlador, pero debe ser diferente de todos los demás nombres bajo esa subclave de tipo.</span><span class="sxs-lookup"><span data-stu-id="f3aec-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="f3aec-254">Establezca el valor predeterminado de la subclave Name en la forma de cadena del GUID del controlador.</span><span class="sxs-lookup"><span data-stu-id="f3aec-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="f3aec-255">En el ejemplo siguiente se muestran las entradas del registro que habilitan los controladores de extensiones de menús contextuales y hojas de propiedades mediante un tipo de archivo. MYP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f3aec-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="f3aec-256">Registrando controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="f3aec-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="f3aec-257">El procedimiento de registro descrito en esta sección debe seguirse para todos los sistemas de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3aec-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="f3aec-258">Sin embargo, con los sistemas posteriores, podría ser necesario un paso adicional.</span><span class="sxs-lookup"><span data-stu-id="f3aec-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="f3aec-259">Dado que estas versiones posteriores de Windows están diseñadas para usarse en un entorno administrado, el acceso al registro se puede restringir administrativamente, lo que requiere un enfoque algo diferente de la instalación que se describe en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="f3aec-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="f3aec-260">Los programas de instalación no suelen escribir directamente en el registro.</span><span class="sxs-lookup"><span data-stu-id="f3aec-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="f3aec-261">En su lugar, el programa de instalación debe realizarse con Windows Installer paquetes.</span><span class="sxs-lookup"><span data-stu-id="f3aec-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="f3aec-262">Estas herramientas garantizan que el software se ejecute correctamente y proporcione acceso a funcionalidades como el registro de clases por usuario.</span><span class="sxs-lookup"><span data-stu-id="f3aec-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="f3aec-263">Los controladores de extensión de Shell se ejecutan en el proceso de Shell.</span><span class="sxs-lookup"><span data-stu-id="f3aec-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="f3aec-264">Dado que se trata de un proceso del sistema, el administrador de un sistema puede limitar los controladores de extensión de Shell a los de una lista aprobada estableciendo el valor de EnforceShellExtensionSecurity de la clave del **Explorador** en 1, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="f3aec-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="f3aec-265">Para colocar un controlador de extensión de Shell en la lista aprobada, cree un valor de **reg \_ SZ** cuyo nombre sea la forma de cadena del GUID del controlador en la subclave **aprobada** .</span><span class="sxs-lookup"><span data-stu-id="f3aec-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="f3aec-266">Por ejemplo, en el ejemplo siguiente se agregan los controladores de *comandos* y *MyPropSheet* a la lista aprobada.</span><span class="sxs-lookup"><span data-stu-id="f3aec-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="f3aec-267">El shell no utiliza el valor asignado al GUID, pero debe establecerse para facilitar la inspección del registro.</span><span class="sxs-lookup"><span data-stu-id="f3aec-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="f3aec-268">La aplicación de instalación puede agregar valores a la subclave **aprobada** solo si la persona que instala la aplicación tiene privilegios suficientes.</span><span class="sxs-lookup"><span data-stu-id="f3aec-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="f3aec-269">Si se produce un error al intentar agregar un controlador de extensión, debe informar al usuario de que se necesitan privilegios administrativos para instalar completamente la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3aec-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="f3aec-270">Si el controlador es esencial para la aplicación, se debe producir un error en la instalación y notificar al usuario que se ponga en contacto con un administrador.</span><span class="sxs-lookup"><span data-stu-id="f3aec-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3aec-271">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3aec-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3aec-272">Inicializar controladores de extensión de Shell</span><span class="sxs-lookup"><span data-stu-id="f3aec-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
