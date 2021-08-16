---
description: En esta sección se describe Windows objetos implementados por el shell.
title: Objetos de shell para scripting y Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858804"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Objetos de shell para scripting y Microsoft Visual Basic

En esta sección se describe Windows objetos implementados por el shell.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br/></td>
<td>Permite a un cliente administrar la configuración de cuota global de disco de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la <a href="didiskquotauser-object.md"><strong>interfaz DIDiskQuotaUser</strong></a> esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Permite a un administrador administrar las propiedades de cuota de disco de un volumen. El sistema de archivos NTFS permite a un administrador administrar el uso de disco en un volumen compartido mediante la asignación de una cantidad especificada de espacio en disco, o límite de <em>cuota,</em>a cada usuario. Puede usar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los usuarios nuevos.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Recibe eventos de registro de ventana de <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows.</strong></a> <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Carpeta</strong></a><br/></td>
<td>Representa una carpeta shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Carpeta2</strong></a><br/></td>
<td>Extiende el objeto <a href="folder.md"><strong>Folder para</strong></a> admitir carpetas sin conexión.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Representa un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Representa la colección de elementos de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Extiende el <a href="folderitems.md"><strong>objeto FolderItems.</strong></a> Admite un método adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Extiende el <a href="folderitems2-object.md"><strong>objeto FolderItems2.</strong></a> Este objeto admite un método y una propiedad adicionales.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Representa un verbo único disponible para un elemento. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Representa la colección de verbos para un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Representa un objeto en el Shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Extiende el <a href="ishelldispatch.md"><strong>objeto IShellDispatch</strong></a> con una variedad de funcionalidades nuevas. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Extiende el <a href="ishelldispatch2-object.md"><strong>objeto IShellDispatch2.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3 admite</strong></a> un nuevo método además de las propiedades y los métodos admitidos por <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Extiende el <a href="ishelldispatch3.md"><strong>objeto IShellDispatch3.</strong></a> Además de las propiedades y los métodos admitidos por <strong>IShellDispatch3,</strong> <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> admite cuatro métodos adicionales. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Extiende el <a href="ishelldispatch4.md"><strong>objeto IShellDispatch4.</strong></a> Además de las propiedades y los métodos admitidos por <strong>IShellDispatch4,</strong> <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> agrega un método que muestra las ventanas abiertas en una pila 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Extiende el <a href="ishelldispatch5.md"><strong>objeto IShellDispatch5.</strong></a> Además de las propiedades y los métodos admitidos por <strong>IShellDispatch5,</strong> <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> agrega un método que muestra el panel Búsqueda de aplicaciones. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> se implementa y se accede a través del <a href="shell.md"><strong>objeto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Extiende el objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> y admite una propiedad adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Extiende el <a href="webwizardhost.md"><strong>objeto WebWizardHost</strong></a> habilitando las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de una cuenta Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Representa los objetos del Shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Extiende el <a href="folderitem.md"><strong>objeto FolderItem.</strong></a> Además de las propiedades y los métodos admitidos <strong>por FolderItem,</strong> <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tiene dos métodos adicionales.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Representa los objetos de una vista y proporciona propiedades y métodos utilizados para obtener información sobre el contenido de la vista.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Reenvía los eventos desencadenados por un objeto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> especificado a los controladores de eventos <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondientes.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Administra los vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>interfaz IShellLink</strong></a> esté disponible para las aplicaciones de scripting. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>Implementado por el Shell para ayudar a crear scripts Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El <a href="shelluihelper.md"><strong>objeto ShellUIHelper</strong></a> no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Representa una colección de las ventanas abiertas que pertenecen al Shell. Los métodos asociados a estos objetos pueden controlar y ejecutar comandos dentro del Shell y obtener otros objetos relacionados con Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Expone métodos que permiten que las páginas HTML hospedadas en una extensión del asistente se comuniquen con el asistente.<br/></td>
</tr>
</tbody>
</table>



 

 

 




