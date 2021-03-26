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
# <a name="scriptable-shell-objects"></a>Objetos de Shell con scripts

El shell de Windows proporciona un conjunto eficaz de objetos de automatización que permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript). Puede usar estos objetos para tener acceso a muchas de las características y cuadros de diálogo del shell. Por ejemplo, puede tener acceso al sistema de archivos, iniciar programas y cambiar la configuración del sistema.

En esta sección se presentan los objetos de Shell que admiten scripts.

-   [Versiones de Shell](#shell-versions)
-   [Crear instancias de objetos de Shell](#instantiating-shell-objects)
    -   [Enlace en tiempo de ejecución](#late-binding)
    -   [Elemento de objeto HTML](#html-object-element)
-   [Objeto de Shell](#shell-object)
    -   [Seguridad](#security)
-   [Objetos de carpeta](#folder-objects)

## <a name="shell-versions"></a>Versiones de Shell

Muchos de los objetos de Shell están disponibles en la [versión 4,71](versions.md) del shell. Otros están disponibles en la versión 5,00 y versiones posteriores. La versión 5,00 estuvo disponible con Windows 2000. En la tabla siguiente se enumeran todos los objetos de Shell en la versión del shell en el que el objeto estuvo disponible.



| Versión 4,71                                            | Versión 5,00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Carpeta**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Carpeta2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**Carpeta**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Crear instancias de objetos de Shell

Para crear instancias de los objetos de Shell en Visual Basic aplicaciones con enlace anticipado, agregue referencias a las siguientes bibliotecas en el proyecto:

-   Microsoft Internet Controls (SHDocVw)
-   Automatización y controles de Microsoft Shell (shell32)

### <a name="late-binding"></a>Enlace en tiempo de ejecución

También puede crear instancias de muchos de los objetos de Shell con enlace en tiempo de ejecución. Este enfoque funciona en Visual Basic aplicaciones y en el script. En el ejemplo siguiente se muestra cómo crear una instancia del objeto de [**Shell**](shell.md) en JScript.


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



En el ejemplo siguiente se muestra cómo crear una instancia del objeto [**Folder**](folder.md) en VBScript.


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



En el ejemplo anterior, *sDir* es la ruta de acceso al objeto de [**carpeta**](folder.md) . Tenga en cuenta que los valores de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.

En la tabla siguiente se muestra el ProgID para cada uno de los objetos de Shell.



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft. DiskQuota. 1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | No se puede enlazar tardíamente                                                                        |
| [**Carpeta**](folder.md)                                | interfaz. Shell \_ Application. Namespace ("...")                                               |
| [**Carpeta2**](folder2-object.md)                       | interfaz. Shell \_ Application. Namespace ("...")                                               |
| [**Carpeta**](folderitem.md)                        | interfaz. Shell \_ Application. Namespace ("..."). Self o Folder. items. Item o Folder. ParseName |
| [**FolderItems**](folderitems.md)                      | Carpeta. Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Carpeta. Items                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell. NameSpace ("..."). Self. Verbs. Item ()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | Carpeta. Verbs o shell. NameSpace ("..."). Self. verbs                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | interfaz. Aplicación de Shell \_                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. NameSpace ("..."). Self. GetLink o shell. NameSpace ("..."). Elementos (). GetLink           |
| [**Shell**](shell.md)                                  | interfaz. Aplicación de Shell \_                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell. NameSpace ("..."). Self o shell. NameSpace ("..."). Elementos ()                           |
| [**ShellFolderView**](shellfolderview.md)              | No se puede enlazar tardíamente                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | No se puede enlazar tardíamente                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell. NameSpace ("..."). Self. GetLink o shell. NameSpace ("..."). Elementos (). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | No se puede enlazar tardíamente                                                                        |
| [**ShellWindows**](shellwindows.md)                    | interfaz. Shell \_ de Windows o ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | No se puede enlazar tardíamente                                                                        |



 

### <a name="html-object-element"></a>Elemento de objeto HTML

También puede usar el elemento de [**objeto**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para crear instancias de objetos de Shell en una página HTML. Para ello, establezca el atributo **ID** del elemento de **objeto** en el nombre de la variable que va a usar en los scripts e identifique el objeto utilizando su número registrado (CLASSID). En el código HTML siguiente se crea una instancia del objeto [**ShellFolderItem**](shellfolderitem-object.md) mediante el elemento de **objeto** .


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



En la tabla siguiente se enumeran todos los objetos de Shell y su identificador de objeto correspondiente.



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Carpeta**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Carpeta2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**Carpeta**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Objeto de Shell

El objeto de [**Shell**](shell.md) representa los objetos del shell. Puede usar los métodos expuestos por el objeto de Shell para:

-   Abra, explore y busque carpetas.
-   Minimizar, restaurar, cascada o mosaico abrir ventanas.
-   Inicie las aplicaciones del panel de control.
-   Cuadros de diálogo de sistema de pantalla.

Es posible que los usuarios estén más familiarizados con los comandos a los que acceden desde el menú **Inicio** y el menú contextual de la barra de tareas. El menú contextual de la barra de tareas aparece cuando los usuarios hacen clic con el botón secundario en la barra de tareas. La siguiente aplicación HTML (HTA) genera una página de inicio con botones que implementan muchos de los métodos del objeto [**Shell**](shell.md) . Algunos de estos métodos implementan características en el menú **Inicio** y en el menú contextual de la barra de tareas.


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



### <a name="security"></a>Seguridad

Como aplicación, una HTA se ejecuta bajo un modelo de seguridad diferente que una página web. Para interactuar con una página web que implementa la funcionalidad de los objetos de Shell, los usuarios deben habilitar la opción **inicializar y generar script de controles ActiveX no marcados como seguros** para la zona de seguridad en la que están viendo la página.

## <a name="folder-objects"></a>Objetos de carpeta

El objeto [**Folder**](folder.md) representa una carpeta de Shell. Puede usar los métodos expuestos por el objeto de carpeta para:

-   Obtener información acerca de una carpeta.
-   Crear subcarpetas.
-   Copie y mueva los objetos de archivo en la carpeta.

El objeto [**carpeta**](folderitem.md) representa un elemento de una carpeta de Shell. Sus propiedades permiten recuperar información sobre el elemento. Puede usar los métodos expuestos por este objeto para ejecutar los verbos de un elemento o recuperar información sobre el objeto [**FolderItemVerbs**](folderitemverbs.md) de un elemento.

El objeto [**FolderItems**](folderitems.md) representa una colección de elementos de una carpeta de Shell. Sus métodos y propiedades le permiten recuperar información sobre la colección.

En el siguiente ejemplo de Visual Basic se muestra la relación entre varios objetos de carpeta y cómo se pueden usar juntos. Cuando el usuario hace clic en el botón de comando denominado **cmdGetPath**, el programa muestra un cuadro de diálogo que permite al usuario seleccionar una carpeta de **mi PC**, donde ssfDRIVES es el valor de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) de **mi PC**. Cuando el usuario elige una carpeta, se muestra la ruta de acceso de la carpeta en el cuadro de texto denominado **txtPath**.


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



En VBScript, esta función es ligeramente diferente porque los valores de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script. En el ejemplo siguiente se muestra el equivalente de VBScript del ejemplo anterior.


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



En el siguiente ejemplo de JScript, que es una traducción directa del ejemplo de VBScript anterior, observe cómo se usan los paréntesis vacíos ' () ' para invocar los [**métodos items y**](folder-items.md) [**Item**](folderitems-item.md) .


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



 

 
