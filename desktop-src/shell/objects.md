---
description: En esta sección se describen los objetos de Windows implementados por el shell.
title: Objetos de Shell para scripting y Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545923"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="0219a-103">Objetos de Shell para scripting y Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0219a-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="0219a-104">En esta sección se describen los objetos de Windows implementados por el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0219a-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0219a-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0219a-106">Tema</span><span class="sxs-lookup"><span data-stu-id="0219a-106">Topic</span></span></th>
<th><span data-ttu-id="0219a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0219a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0219a-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-109">Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="0219a-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="0219a-110">Este objeto hace que la funcionalidad esencial de la interfaz <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0219a-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-112">Permite que un administrador administre las propiedades de cuota de disco de un volumen.</span><span class="sxs-lookup"><span data-stu-id="0219a-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="0219a-113">El sistema de archivos NTFS permite que un administrador administre el uso de disco en un volumen compartido asignando una cantidad especificada de espacio en disco, o <em>límite de cuota</em>, a cada usuario.</span><span class="sxs-lookup"><span data-stu-id="0219a-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="0219a-114">Puede utilizar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los nuevos usuarios.</span><span class="sxs-lookup"><span data-stu-id="0219a-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-116">Recibe los eventos de registro de la ventana <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-117"><a href="folder.md"><strong>Carpeta</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-118">Representa una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-118">Represents a Shell folder.</span></span> <span data-ttu-id="0219a-119">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0219a-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-120"><a href="folder2-object.md"><strong>Carpeta2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-121">Extiende el objeto de <a href="folder.md"><strong>carpeta</strong></a> para admitir carpetas sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0219a-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-122"><a href="folderitem.md"><strong>Carpeta</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-123">Representa un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="0219a-124">Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="0219a-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-126">Representa la colección de elementos de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="0219a-127">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="0219a-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-129">Extiende el objeto <a href="folderitems.md"><strong>FolderItems</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="0219a-130">Admite un método adicional.</span><span class="sxs-lookup"><span data-stu-id="0219a-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-132">Extiende el objeto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="0219a-133">Este objeto admite un método y una propiedad adicionales.</span><span class="sxs-lookup"><span data-stu-id="0219a-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-135">Representa un único Verbo disponible para un elemento.</span><span class="sxs-lookup"><span data-stu-id="0219a-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="0219a-136">Este objeto contiene propiedades y métodos que permiten recuperar información sobre el verbo.</span><span class="sxs-lookup"><span data-stu-id="0219a-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-138">Representa la colección de verbos para un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="0219a-139">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="0219a-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-141">Representa un objeto en el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-141">Represents an object in the Shell.</span></span> <span data-ttu-id="0219a-142">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="0219a-143">También hay métodos para obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-146">Extiende el objeto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> con una variedad de nuevas funciones.</span><span class="sxs-lookup"><span data-stu-id="0219a-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-149">Extiende el objeto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="0219a-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> admite un nuevo método además de las propiedades y los métodos admitidos por <strong>IShellDispatch2</strong>.</span><span class="sxs-lookup"><span data-stu-id="0219a-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-153">Extiende el objeto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="0219a-154">Además de las propiedades y los métodos admitidos por <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> admite cuatro métodos adicionales.</span><span class="sxs-lookup"><span data-stu-id="0219a-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-157">Extiende el objeto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="0219a-158">Además de las propiedades y los métodos admitidos por <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> agrega un método que muestra ventanas abiertas en una pila 3D.</span><span class="sxs-lookup"><span data-stu-id="0219a-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-161">Extiende el objeto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="0219a-162">Además de las propiedades y los métodos admitidos por <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> agrega un método que muestra el panel de búsqueda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0219a-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="0219a-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-165">Extiende el objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> y admite una propiedad adicional.</span><span class="sxs-lookup"><span data-stu-id="0219a-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-167">Extiende el objeto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> habilitando las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0219a-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-169">Representa los objetos del shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="0219a-170">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="0219a-171">También hay métodos para obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-173">Extiende el objeto <a href="folderitem.md"><strong>carpeta</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0219a-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="0219a-174">Además de las propiedades y los métodos admitidos por <strong>carpeta</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tiene dos métodos adicionales.</span><span class="sxs-lookup"><span data-stu-id="0219a-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-176">Representa los objetos en una vista y proporciona propiedades y métodos que se usan para obtener información sobre el contenido de la vista.</span><span class="sxs-lookup"><span data-stu-id="0219a-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-178">Reenvía los eventos desencadenados por un objeto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> especificado a los controladores de eventos <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondientes.</span><span class="sxs-lookup"><span data-stu-id="0219a-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-180">Administra vínculos de Shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-180">Manages Shell links.</span></span> <span data-ttu-id="0219a-181">Este objeto hace que gran parte de la funcionalidad de la interfaz <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> esté disponible para las aplicaciones de scripting.</span><span class="sxs-lookup"><span data-stu-id="0219a-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-183">Implementado por el shell para ayudar a los desarrolladores de script y Visual Basic a usar algunas de las características disponibles en el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="0219a-184">El objeto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> no tiene propiedades ni eventos.</span><span class="sxs-lookup"><span data-stu-id="0219a-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="0219a-185">Se proporcionan métodos para agregar elementos al shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0219a-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-187">Representa una colección de las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="0219a-188">Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="0219a-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0219a-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="0219a-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="0219a-190">Expone métodos que permiten a las páginas HTML que se hospedan en una extensión de asistente comunicarse con el asistente.</span><span class="sxs-lookup"><span data-stu-id="0219a-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




