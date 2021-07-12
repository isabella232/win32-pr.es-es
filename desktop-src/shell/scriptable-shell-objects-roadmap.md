---
description: El shell de Windows proporciona un conjunto eficaz de objetos de automatización que le permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript). Puede usar estos objetos para acceder a muchas de las características y cuadros de diálogo del shell. Por ejemplo, puede acceder al sistema de archivos, iniciar programas y cambiar la configuración del sistema.
title: Objetos de shell que pueden incluirse en scripts
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581783"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="477ed-105">Objetos de shell que pueden incluirse en scripts</span><span class="sxs-lookup"><span data-stu-id="477ed-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="477ed-106">El shell de Windows proporciona un conjunto eficaz de objetos de automatización que le permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="477ed-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="477ed-107">Puede usar estos objetos para acceder a muchas de las características y cuadros de diálogo del shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="477ed-108">Por ejemplo, puede acceder al sistema de archivos, iniciar programas y cambiar la configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="477ed-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="477ed-109">En esta sección se presentan los objetos shell que pueden incluirse en scripts.</span><span class="sxs-lookup"><span data-stu-id="477ed-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="477ed-110">Versiones del shell</span><span class="sxs-lookup"><span data-stu-id="477ed-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="477ed-111">Creación de instancias de objetos de shell</span><span class="sxs-lookup"><span data-stu-id="477ed-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="477ed-112">Enlace en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="477ed-113">Elemento HTML OBJECT</span><span class="sxs-lookup"><span data-stu-id="477ed-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="477ed-114">Objeto shell</span><span class="sxs-lookup"><span data-stu-id="477ed-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="477ed-115">Seguridad</span><span class="sxs-lookup"><span data-stu-id="477ed-115">Security</span></span>](#security)
-   [<span data-ttu-id="477ed-116">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="477ed-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="477ed-117">Versiones del shell</span><span class="sxs-lookup"><span data-stu-id="477ed-117">Shell Versions</span></span>

<span data-ttu-id="477ed-118">Muchos de los objetos de Shell están disponibles [en la versión 4.71](versions.md) del shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="477ed-119">Otras están disponibles en la versión 5.00 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="477ed-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="477ed-120">La versión 5.00 está disponible con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="477ed-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="477ed-121">En la tabla siguiente se muestra cada objeto shell en la versión del shell en la que el objeto empezó a estar disponible.</span><span class="sxs-lookup"><span data-stu-id="477ed-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="477ed-122">Versión 4.71</span><span class="sxs-lookup"><span data-stu-id="477ed-122">Version 4.71</span></span>                                            | <span data-ttu-id="477ed-123">Versión 5.00</span><span class="sxs-lookup"><span data-stu-id="477ed-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="477ed-124">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="477ed-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="477ed-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="477ed-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="477ed-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="477ed-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="477ed-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="477ed-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="477ed-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="477ed-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="477ed-129">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="477ed-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="477ed-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="477ed-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="477ed-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="477ed-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="477ed-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="477ed-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="477ed-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="477ed-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="477ed-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="477ed-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="477ed-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="477ed-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="477ed-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="477ed-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="477ed-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="477ed-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="477ed-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="477ed-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="477ed-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="477ed-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="477ed-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="477ed-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="477ed-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="477ed-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="477ed-143">Creación de instancias de objetos de shell</span><span class="sxs-lookup"><span data-stu-id="477ed-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="477ed-144">Para crear instancias de los objetos de Shell Visual Basic aplicaciones con enlace anticipado, agregue referencias a las siguientes bibliotecas en el proyecto:</span><span class="sxs-lookup"><span data-stu-id="477ed-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="477ed-145">Controles de Internet de Microsoft (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="477ed-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="477ed-146">Controles y automatización de Microsoft Shell (Shell32)</span><span class="sxs-lookup"><span data-stu-id="477ed-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="477ed-147">Enlace en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-147">Late Binding</span></span>

<span data-ttu-id="477ed-148">También puede crear instancias de muchos de los objetos de Shell con enlace en tiempo de tarde.</span><span class="sxs-lookup"><span data-stu-id="477ed-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="477ed-149">Este enfoque funciona en Visual Basic y en script.</span><span class="sxs-lookup"><span data-stu-id="477ed-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="477ed-150">En el ejemplo siguiente se muestra cómo crear una instancia del objeto [**Shell**](shell.md) en JScript.</span><span class="sxs-lookup"><span data-stu-id="477ed-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="477ed-151">En el ejemplo siguiente se muestra cómo crear una instancia del [**objeto Folder**](folder.md) en VBScript.</span><span class="sxs-lookup"><span data-stu-id="477ed-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="477ed-152">En el ejemplo anterior, *sDir es* la ruta de acceso al [**objeto Folder.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="477ed-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="477ed-153">Tenga en cuenta [**que los valores de enumeración ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.</span><span class="sxs-lookup"><span data-stu-id="477ed-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="477ed-154">El ProgID de cada uno de los objetos de Shell se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="477ed-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="477ed-155">Object</span><span class="sxs-lookup"><span data-stu-id="477ed-155">Object</span></span>                                                  | <span data-ttu-id="477ed-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="477ed-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="477ed-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="477ed-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="477ed-158">Microsoft.DiskQuota.1</span><span class="sxs-lookup"><span data-stu-id="477ed-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="477ed-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="477ed-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="477ed-160">No se puede enlazar en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="477ed-161">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="477ed-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="477ed-162">Cáscara. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="477ed-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="477ed-163">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="477ed-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="477ed-164">Cáscara. Shell \_ Application.NameSpace("...")</span><span class="sxs-lookup"><span data-stu-id="477ed-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="477ed-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="477ed-166">Cáscara. Shell \_ Application.NameSpace("..."). Self o Folder.Items.Item o Folder.ParseName</span><span class="sxs-lookup"><span data-stu-id="477ed-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="477ed-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="477ed-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="477ed-168">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="477ed-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="477ed-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="477ed-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="477ed-170">Folder.Items</span><span class="sxs-lookup"><span data-stu-id="477ed-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="477ed-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="477ed-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="477ed-172">Shell.NameSpace("..."). Self.Verbs.Item()</span><span class="sxs-lookup"><span data-stu-id="477ed-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="477ed-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="477ed-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="477ed-174">FolderItem.Verbs o Shell.NameSpace("..."). Self.Verbs</span><span class="sxs-lookup"><span data-stu-id="477ed-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="477ed-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="477ed-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="477ed-176">Cáscara. Aplicación de \_ shell</span><span class="sxs-lookup"><span data-stu-id="477ed-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="477ed-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="477ed-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="477ed-178">Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="477ed-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="477ed-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="477ed-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="477ed-180">Cáscara. Aplicación de \_ shell</span><span class="sxs-lookup"><span data-stu-id="477ed-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="477ed-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="477ed-182">Shell.NameSpace("..."). Self o Shell.NameSpace("..."). Items()</span><span class="sxs-lookup"><span data-stu-id="477ed-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="477ed-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="477ed-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="477ed-184">No se puede enlazar en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="477ed-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="477ed-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="477ed-186">No se puede enlazar en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="477ed-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="477ed-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="477ed-188">Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink</span><span class="sxs-lookup"><span data-stu-id="477ed-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="477ed-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="477ed-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="477ed-190">No se puede enlazar en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="477ed-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="477ed-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="477ed-192">Cáscara. Shell \_ Windows o ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="477ed-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="477ed-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="477ed-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="477ed-194">No se puede enlazar en tiempo de tarde</span><span class="sxs-lookup"><span data-stu-id="477ed-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="477ed-195">Elemento HTML OBJECT</span><span class="sxs-lookup"><span data-stu-id="477ed-195">HTML OBJECT Element</span></span>

<span data-ttu-id="477ed-196">También puede usar el elemento [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para crear instancias de objetos de Shell en una página HTML.</span><span class="sxs-lookup"><span data-stu-id="477ed-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="477ed-197">Para ello, establezca el atributo  ID del elemento **OBJECT** en el nombre de variable que usará en los scripts e identifique el objeto con su número registrado (CLASSID).</span><span class="sxs-lookup"><span data-stu-id="477ed-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="477ed-198">El siguiente código HTML crea una instancia del [**objeto ShellFolderItem**](shellfolderitem-object.md) mediante el **elemento OBJECT.**</span><span class="sxs-lookup"><span data-stu-id="477ed-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="477ed-199">En la tabla siguiente se muestra cada objeto de Shell y su CLASSID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="477ed-199">The following table lists each Shell object and its respective CLASSID.</span></span>



| <span data-ttu-id="477ed-200">Objeto shell</span><span class="sxs-lookup"><span data-stu-id="477ed-200">Shell object</span></span>                                           | <span data-ttu-id="477ed-201">Classid</span><span class="sxs-lookup"><span data-stu-id="477ed-201">CLASSID</span></span>                              |
|--------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="477ed-202">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="477ed-202">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="477ed-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="477ed-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="477ed-204">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="477ed-204">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="477ed-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="477ed-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="477ed-206">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="477ed-206">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="477ed-207">QUEBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="477ed-207">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="477ed-208">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="477ed-208">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="477ed-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="477ed-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="477ed-210">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-210">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="477ed-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="477ed-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="477ed-212">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="477ed-212">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="477ed-213">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="477ed-213">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="477ed-214">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="477ed-214">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="477ed-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="477ed-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="477ed-216">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="477ed-216">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="477ed-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="477ed-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="477ed-218">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="477ed-218">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="477ed-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="477ed-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="477ed-220">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="477ed-220">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="477ed-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="477ed-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="477ed-222">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="477ed-222">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="477ed-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="477ed-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="477ed-224">**Shell**</span><span class="sxs-lookup"><span data-stu-id="477ed-224">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="477ed-225">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="477ed-225">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="477ed-226">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="477ed-226">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="477ed-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="477ed-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="477ed-228">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="477ed-228">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="477ed-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="477ed-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="477ed-230">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="477ed-230">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="477ed-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="477ed-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="477ed-232">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="477ed-232">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="477ed-233">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="477ed-233">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="477ed-234">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="477ed-234">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="477ed-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="477ed-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="477ed-236">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="477ed-236">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="477ed-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="477ed-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="477ed-238">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="477ed-238">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="477ed-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="477ed-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="477ed-240">Objeto shell</span><span class="sxs-lookup"><span data-stu-id="477ed-240">Shell Object</span></span>

<span data-ttu-id="477ed-241">El [**objeto**](shell.md) Shell representa los objetos del shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-241">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="477ed-242">Puede usar los métodos expuestos por el objeto shell para:</span><span class="sxs-lookup"><span data-stu-id="477ed-242">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="477ed-243">Abra, explore y busque carpetas.</span><span class="sxs-lookup"><span data-stu-id="477ed-243">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="477ed-244">Minimice, restaure, en cascada o abra ventanas de mosaico.</span><span class="sxs-lookup"><span data-stu-id="477ed-244">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="477ed-245">Inicie Panel de control aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="477ed-245">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="477ed-246">Mostrar cuadros de diálogo del sistema.</span><span class="sxs-lookup"><span data-stu-id="477ed-246">Display system dialog boxes.</span></span>

<span data-ttu-id="477ed-247">Los usuarios quizás estén más familiarizados con los comandos a los que acceden desde el **menú** Inicio y el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="477ed-247">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="477ed-248">El menú contextual de la barra de tareas aparece cuando los usuarios hacen clic con el botón derecho en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="477ed-248">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="477ed-249">La siguiente aplicación HTML (HTA) genera una página de [](shell.md) inicio con botones que implementan muchos de los métodos del objeto shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-249">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="477ed-250">Algunos de estos métodos implementan características en el **menú** Inicio y en el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="477ed-250">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="477ed-251">Seguridad</span><span class="sxs-lookup"><span data-stu-id="477ed-251">Security</span></span>

<span data-ttu-id="477ed-252">Como aplicación, un HTA se ejecuta con un modelo de seguridad diferente al de una página web.</span><span class="sxs-lookup"><span data-stu-id="477ed-252">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="477ed-253">Para interactuar con una página web que implementa la funcionalidad de los objetos de Shell, los usuarios deben habilitar la opción Inicializar y incluir en script los controles **ActiveX** no marcados como seguros para la zona de seguridad en la que están viendo la página.</span><span class="sxs-lookup"><span data-stu-id="477ed-253">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="477ed-254">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="477ed-254">Folder Objects</span></span>

<span data-ttu-id="477ed-255">El [**objeto Folder**](folder.md) representa una carpeta shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-255">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="477ed-256">Puede usar los métodos expuestos por el objeto Folder para:</span><span class="sxs-lookup"><span data-stu-id="477ed-256">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="477ed-257">Obtenga información sobre una carpeta.</span><span class="sxs-lookup"><span data-stu-id="477ed-257">Get information about a folder.</span></span>
-   <span data-ttu-id="477ed-258">Cree subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="477ed-258">Create subfolders.</span></span>
-   <span data-ttu-id="477ed-259">Copie y mueva objetos de archivo a la carpeta .</span><span class="sxs-lookup"><span data-stu-id="477ed-259">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="477ed-260">El [**objeto FolderItem**](folderitem.md) representa un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-260">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="477ed-261">Sus propiedades permiten recuperar información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="477ed-261">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="477ed-262">Puede usar los métodos expuestos por este objeto para ejecutar los verbos de un elemento o para recuperar información sobre el objeto [**FolderItemVerbs**](folderitemverbs.md) de un elemento.</span><span class="sxs-lookup"><span data-stu-id="477ed-262">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="477ed-263">El [**objeto FolderItems**](folderitems.md) representa una colección de elementos de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="477ed-263">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="477ed-264">Sus métodos y propiedades permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="477ed-264">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="477ed-265">En el Visual Basic siguiente se muestra la relación entre varios de los objetos de carpeta y cómo se pueden usar juntos.</span><span class="sxs-lookup"><span data-stu-id="477ed-265">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="477ed-266">Cuando el usuario hace clic en el botón de comando denominado **cmdGetPath**, el programa muestra un cuadro de diálogo que permite al usuario seleccionar una carpeta de **Mi PC**, donde ssfDRIVES es el valor de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) **para Mi PC**.</span><span class="sxs-lookup"><span data-stu-id="477ed-266">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="477ed-267">Cuando el usuario elige una carpeta, la ruta de acceso de la carpeta se muestra en el cuadro de texto denominado **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="477ed-267">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="477ed-268">En VBScript, esta función es ligeramente diferente porque los valores de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.</span><span class="sxs-lookup"><span data-stu-id="477ed-268">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="477ed-269">En el ejemplo siguiente se muestra el equivalente de VBScript del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="477ed-269">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="477ed-270">En el ejemplo JScript siguiente, que es una traducción directa del ejemplo de VBScript anterior, observe cómo se usan los paréntesis vacíos '()' para invocar los métodos [**Items**](folder-items.md) y [**Item.**](folderitems-item.md)</span><span class="sxs-lookup"><span data-stu-id="477ed-270">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
