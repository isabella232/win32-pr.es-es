---
description: El shell de Windows proporciona un conjunto eficaz de objetos de automatización que permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript). Puede usar estos objetos para tener acceso a muchas de las características y cuadros de diálogo del shell. Por ejemplo, puede tener acceso al sistema de archivos, iniciar programas y cambiar la configuración del sistema.
title: Objetos de Shell con scripts
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985894"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="75eae-105">Objetos de Shell con scripts</span><span class="sxs-lookup"><span data-stu-id="75eae-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="75eae-106">El shell de Windows proporciona un conjunto eficaz de objetos de automatización que permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="75eae-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="75eae-107">Puede usar estos objetos para tener acceso a muchas de las características y cuadros de diálogo del shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="75eae-108">Por ejemplo, puede tener acceso al sistema de archivos, iniciar programas y cambiar la configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="75eae-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="75eae-109">En esta sección se presentan los objetos de Shell que admiten scripts.</span><span class="sxs-lookup"><span data-stu-id="75eae-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="75eae-110">Versiones de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="75eae-111">Crear instancias de objetos de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="75eae-112">Enlace en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="75eae-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="75eae-113">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="75eae-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="75eae-114">Objeto de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="75eae-115">Seguridad</span><span class="sxs-lookup"><span data-stu-id="75eae-115">Security</span></span>](#security)
-   [<span data-ttu-id="75eae-116">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="75eae-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="75eae-117">Versiones de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-117">Shell Versions</span></span>

<span data-ttu-id="75eae-118">Muchos de los objetos de Shell están disponibles en la [versión 4,71](versions.md) del shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="75eae-119">Otros están disponibles en la versión 5,00 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75eae-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="75eae-120">La versión 5,00 estuvo disponible con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="75eae-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="75eae-121">En la tabla siguiente se enumeran todos los objetos de Shell en la versión del shell en el que el objeto estuvo disponible.</span><span class="sxs-lookup"><span data-stu-id="75eae-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="75eae-122">Versión 4,71</span><span class="sxs-lookup"><span data-stu-id="75eae-122">Version 4.71</span></span>                                            | <span data-ttu-id="75eae-123">Versión 5,00</span><span class="sxs-lookup"><span data-stu-id="75eae-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="75eae-124">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="75eae-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="75eae-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="75eae-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="75eae-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="75eae-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="75eae-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="75eae-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="75eae-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="75eae-129">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="75eae-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="75eae-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="75eae-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="75eae-131">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="75eae-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="75eae-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="75eae-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="75eae-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="75eae-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="75eae-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="75eae-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="75eae-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="75eae-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="75eae-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="75eae-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="75eae-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="75eae-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="75eae-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="75eae-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="75eae-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="75eae-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="75eae-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="75eae-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="75eae-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="75eae-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="75eae-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="75eae-143">Crear instancias de objetos de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="75eae-144">Para crear instancias de los objetos de Shell en Visual Basic aplicaciones con enlace anticipado, agregue referencias a las siguientes bibliotecas en el proyecto:</span><span class="sxs-lookup"><span data-stu-id="75eae-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="75eae-145">Microsoft Internet Controls (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="75eae-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="75eae-146">Automatización y controles de Microsoft Shell (shell32)</span><span class="sxs-lookup"><span data-stu-id="75eae-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="75eae-147">Enlace en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="75eae-147">Late Binding</span></span>

<span data-ttu-id="75eae-148">También puede crear instancias de muchos de los objetos de Shell con enlace en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="75eae-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="75eae-149">Este enfoque funciona en Visual Basic aplicaciones y en el script.</span><span class="sxs-lookup"><span data-stu-id="75eae-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="75eae-150">En el ejemplo siguiente se muestra cómo crear una instancia del objeto de [**Shell**](shell.md) en JScript.</span><span class="sxs-lookup"><span data-stu-id="75eae-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


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



<span data-ttu-id="75eae-151">En el ejemplo siguiente se muestra cómo crear una instancia del objeto [**Folder**](folder.md) en VBScript.</span><span class="sxs-lookup"><span data-stu-id="75eae-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


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



<span data-ttu-id="75eae-152">En el ejemplo anterior, *sDir* es la ruta de acceso al objeto de [**carpeta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="75eae-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="75eae-153">Tenga en cuenta que los valores de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.</span><span class="sxs-lookup"><span data-stu-id="75eae-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="75eae-154">En la tabla siguiente se muestra el ProgID para cada uno de los objetos de Shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="75eae-155">Object</span><span class="sxs-lookup"><span data-stu-id="75eae-155">Object</span></span>                                                  | <span data-ttu-id="75eae-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="75eae-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="75eae-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="75eae-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="75eae-158">Microsoft. DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="75eae-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="75eae-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="75eae-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="75eae-160">No se puede enlazar tardíamente</span><span class="sxs-lookup"><span data-stu-id="75eae-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="75eae-161">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="75eae-162">interfaz. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="75eae-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="75eae-163">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="75eae-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="75eae-164">interfaz. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="75eae-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="75eae-165">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="75eae-166">interfaz. Shell \_ Application. Namespace ("..."). Self o Folder. items. Item o Folder. ParseName</span><span class="sxs-lookup"><span data-stu-id="75eae-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="75eae-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="75eae-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="75eae-168">Carpeta. Items</span><span class="sxs-lookup"><span data-stu-id="75eae-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="75eae-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="75eae-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="75eae-170">Carpeta. Items</span><span class="sxs-lookup"><span data-stu-id="75eae-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="75eae-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="75eae-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="75eae-172">Shell. NameSpace ("..."). Self. Verbs. Item ()</span><span class="sxs-lookup"><span data-stu-id="75eae-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="75eae-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="75eae-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="75eae-174">Carpeta. Verbs o shell. NameSpace ("..."). Self. verbs</span><span class="sxs-lookup"><span data-stu-id="75eae-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="75eae-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="75eae-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="75eae-176">interfaz. Aplicación de Shell \_</span><span class="sxs-lookup"><span data-stu-id="75eae-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="75eae-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="75eae-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="75eae-178">Shell. NameSpace ("..."). Self. GetLink o shell. NameSpace ("..."). Elementos (). GetLink</span><span class="sxs-lookup"><span data-stu-id="75eae-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="75eae-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="75eae-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="75eae-180">interfaz. Aplicación de Shell \_</span><span class="sxs-lookup"><span data-stu-id="75eae-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="75eae-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="75eae-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="75eae-182">Shell. NameSpace ("..."). Self o shell. NameSpace ("..."). Elementos ()</span><span class="sxs-lookup"><span data-stu-id="75eae-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="75eae-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="75eae-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="75eae-184">No se puede enlazar tardíamente</span><span class="sxs-lookup"><span data-stu-id="75eae-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="75eae-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="75eae-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="75eae-186">No se puede enlazar tardíamente</span><span class="sxs-lookup"><span data-stu-id="75eae-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="75eae-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="75eae-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="75eae-188">Shell. NameSpace ("..."). Self. GetLink o shell. NameSpace ("..."). Elementos (). GetLink</span><span class="sxs-lookup"><span data-stu-id="75eae-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="75eae-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="75eae-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="75eae-190">No se puede enlazar tardíamente</span><span class="sxs-lookup"><span data-stu-id="75eae-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="75eae-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="75eae-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="75eae-192">interfaz. Shell \_ de Windows o ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="75eae-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="75eae-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="75eae-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="75eae-194">No se puede enlazar tardíamente</span><span class="sxs-lookup"><span data-stu-id="75eae-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="75eae-195">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="75eae-195">HTML OBJECT Element</span></span>

<span data-ttu-id="75eae-196">También puede usar el elemento de [**objeto**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para crear instancias de objetos de Shell en una página HTML.</span><span class="sxs-lookup"><span data-stu-id="75eae-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="75eae-197">Para ello, establezca el atributo **ID** del elemento de **objeto** en el nombre de la variable que va a usar en los scripts e identifique el objeto utilizando su número registrado (CLASSID).</span><span class="sxs-lookup"><span data-stu-id="75eae-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="75eae-198">En el código HTML siguiente se crea una instancia del objeto [**ShellFolderItem**](shellfolderitem-object.md) mediante el elemento de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="75eae-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="75eae-199">En la tabla siguiente se enumeran todos los objetos de Shell y su identificador de objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="75eae-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="75eae-200">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="75eae-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="75eae-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="75eae-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="75eae-202">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="75eae-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="75eae-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="75eae-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="75eae-204">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="75eae-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="75eae-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="75eae-206">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="75eae-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="75eae-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="75eae-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="75eae-208">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="75eae-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="75eae-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="75eae-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="75eae-210">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="75eae-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="75eae-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="75eae-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="75eae-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="75eae-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="75eae-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="75eae-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="75eae-214">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="75eae-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="75eae-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="75eae-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="75eae-216">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="75eae-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="75eae-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="75eae-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="75eae-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="75eae-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="75eae-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="75eae-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="75eae-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="75eae-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="75eae-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="75eae-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="75eae-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="75eae-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="75eae-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="75eae-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="75eae-224">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="75eae-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="75eae-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="75eae-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="75eae-226">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="75eae-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="75eae-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="75eae-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="75eae-228">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="75eae-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="75eae-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="75eae-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="75eae-230">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="75eae-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="75eae-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="75eae-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="75eae-232">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="75eae-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="75eae-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="75eae-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="75eae-234">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="75eae-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="75eae-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="75eae-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="75eae-236">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="75eae-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="75eae-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="75eae-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="75eae-238">Objeto de Shell</span><span class="sxs-lookup"><span data-stu-id="75eae-238">Shell Object</span></span>

<span data-ttu-id="75eae-239">El objeto de [**Shell**](shell.md) representa los objetos del shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="75eae-240">Puede usar los métodos expuestos por el objeto de Shell para:</span><span class="sxs-lookup"><span data-stu-id="75eae-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="75eae-241">Abra, explore y busque carpetas.</span><span class="sxs-lookup"><span data-stu-id="75eae-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="75eae-242">Minimizar, restaurar, cascada o mosaico abrir ventanas.</span><span class="sxs-lookup"><span data-stu-id="75eae-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="75eae-243">Inicie las aplicaciones del panel de control.</span><span class="sxs-lookup"><span data-stu-id="75eae-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="75eae-244">Cuadros de diálogo de sistema de pantalla.</span><span class="sxs-lookup"><span data-stu-id="75eae-244">Display system dialog boxes.</span></span>

<span data-ttu-id="75eae-245">Es posible que los usuarios estén más familiarizados con los comandos a los que acceden desde el menú **Inicio** y el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="75eae-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="75eae-246">El menú contextual de la barra de tareas aparece cuando los usuarios hacen clic con el botón secundario en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="75eae-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="75eae-247">La siguiente aplicación HTML (HTA) genera una página de inicio con botones que implementan muchos de los métodos del objeto [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="75eae-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="75eae-248">Algunos de estos métodos implementan características en el menú **Inicio** y en el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="75eae-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


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



### <a name="security"></a><span data-ttu-id="75eae-249">Seguridad</span><span class="sxs-lookup"><span data-stu-id="75eae-249">Security</span></span>

<span data-ttu-id="75eae-250">Como aplicación, una HTA se ejecuta bajo un modelo de seguridad diferente que una página web.</span><span class="sxs-lookup"><span data-stu-id="75eae-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="75eae-251">Para interactuar con una página web que implementa la funcionalidad de los objetos de Shell, los usuarios deben habilitar la opción **inicializar y generar script de controles ActiveX no marcados como seguros** para la zona de seguridad en la que están viendo la página.</span><span class="sxs-lookup"><span data-stu-id="75eae-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="75eae-252">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="75eae-252">Folder Objects</span></span>

<span data-ttu-id="75eae-253">El objeto [**Folder**](folder.md) representa una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="75eae-254">Puede usar los métodos expuestos por el objeto de carpeta para:</span><span class="sxs-lookup"><span data-stu-id="75eae-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="75eae-255">Obtener información acerca de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="75eae-255">Get information about a folder.</span></span>
-   <span data-ttu-id="75eae-256">Crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="75eae-256">Create subfolders.</span></span>
-   <span data-ttu-id="75eae-257">Copie y mueva los objetos de archivo en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="75eae-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="75eae-258">El objeto [**carpeta**](folderitem.md) representa un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="75eae-259">Sus propiedades permiten recuperar información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="75eae-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="75eae-260">Puede usar los métodos expuestos por este objeto para ejecutar los verbos de un elemento o recuperar información sobre el objeto [**FolderItemVerbs**](folderitemverbs.md) de un elemento.</span><span class="sxs-lookup"><span data-stu-id="75eae-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="75eae-261">El objeto [**FolderItems**](folderitems.md) representa una colección de elementos de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="75eae-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="75eae-262">Sus métodos y propiedades le permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="75eae-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="75eae-263">En el siguiente ejemplo de Visual Basic se muestra la relación entre varios objetos de carpeta y cómo se pueden usar juntos.</span><span class="sxs-lookup"><span data-stu-id="75eae-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="75eae-264">Cuando el usuario hace clic en el botón de comando denominado **cmdGetPath**, el programa muestra un cuadro de diálogo que permite al usuario seleccionar una carpeta de **mi PC**, donde ssfDRIVES es el valor de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) de **mi PC**.</span><span class="sxs-lookup"><span data-stu-id="75eae-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="75eae-265">Cuando el usuario elige una carpeta, se muestra la ruta de acceso de la carpeta en el cuadro de texto denominado **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="75eae-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


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



<span data-ttu-id="75eae-266">En VBScript, esta función es ligeramente diferente porque los valores de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.</span><span class="sxs-lookup"><span data-stu-id="75eae-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="75eae-267">En el ejemplo siguiente se muestra el equivalente de VBScript del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="75eae-267">The following example shows the VBScript equivalent of the previous example.</span></span>


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



<span data-ttu-id="75eae-268">En el siguiente ejemplo de JScript, que es una traducción directa del ejemplo de VBScript anterior, observe cómo se usan los paréntesis vacíos ' () ' para invocar los [**métodos items y**](folder-items.md) [**Item**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="75eae-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


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



 

 
