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
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Objetos de Shell para scripting y Microsoft Visual Basic

En esta sección se describen los objetos de Windows implementados por el shell.

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
<td>Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Permite que un administrador administre las propiedades de cuota de disco de un volumen. El sistema de archivos NTFS permite que un administrador administre el uso de disco en un volumen compartido asignando una cantidad especificada de espacio en disco, o <em>límite de cuota</em>, a cada usuario. Puede utilizar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los nuevos usuarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Recibe los eventos de registro de la ventana <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Carpeta</strong></a><br/></td>
<td>Representa una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Carpeta2</strong></a><br/></td>
<td>Extiende el objeto de <a href="folder.md"><strong>carpeta</strong></a> para admitir carpetas sin conexión.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>Carpeta</strong></a><br/></td>
<td>Representa un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Representa la colección de elementos de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Extiende el objeto <a href="folderitems.md"><strong>FolderItems</strong></a> . Admite un método adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Extiende el objeto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Este objeto admite un método y una propiedad adicionales.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Representa un único Verbo disponible para un elemento. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Representa la colección de verbos para un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Representa un objeto en el shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con el shell. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Extiende el objeto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> con una variedad de nuevas funciones. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Extiende el objeto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> admite un nuevo método además de las propiedades y los métodos admitidos por <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Extiende el objeto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . Además de las propiedades y los métodos admitidos por <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> admite cuatro métodos adicionales. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Extiende el objeto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . Además de las propiedades y los métodos admitidos por <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> agrega un método que muestra ventanas abiertas en una pila 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Extiende el objeto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . Además de las propiedades y los métodos admitidos por <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> agrega un método que muestra el panel de búsqueda de aplicaciones. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> se implementa y se obtiene acceso a él a través del objeto de <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Extiende el objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> y admite una propiedad adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Extiende el objeto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> habilitando las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Representa los objetos del shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con el shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Extiende el objeto <a href="folderitem.md"><strong>carpeta</strong></a> . Además de las propiedades y los métodos admitidos por <strong>carpeta</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tiene dos métodos adicionales.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Representa los objetos en una vista y proporciona propiedades y métodos que se usan para obtener información sobre el contenido de la vista.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Reenvía los eventos desencadenados por un objeto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> especificado a los controladores de eventos <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondientes.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Administra vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la interfaz <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> esté disponible para las aplicaciones de scripting. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>Implementado por el shell para ayudar a los desarrolladores de script y Visual Basic a usar algunas de las características disponibles en el shell. El objeto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Representa una colección de las ventanas abiertas que pertenecen al shell. Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Expone métodos que permiten a las páginas HTML que se hospedan en una extensión de asistente comunicarse con el asistente.<br/></td>
</tr>
</tbody>
</table>



 

 

 




