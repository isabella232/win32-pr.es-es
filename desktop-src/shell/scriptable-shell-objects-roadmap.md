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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248030"
---
# <a name="scriptable-shell-objects"></a>Objetos de shell que pueden incluirse en scripts

El shell de Windows proporciona un conjunto eficaz de objetos de automatización que le permiten programar el shell con Microsoft Visual Basic y lenguajes de scripting como Microsoft JScript (compatible con la especificación del lenguaje ECMA 262) y Microsoft Visual Basic Scripting Edition (VBScript). Puede usar estos objetos para acceder a muchas de las características y cuadros de diálogo del shell. Por ejemplo, puede acceder al sistema de archivos, iniciar programas y cambiar la configuración del sistema.

En esta sección se presentan los objetos shell que pueden incluirse en scripts.

-   [Versiones del shell](#shell-versions)
-   [Creación de instancias de objetos de shell](#instantiating-shell-objects)
    -   [Enlace en tiempo de tarde](#late-binding)
    -   [Elemento HTML OBJECT](#html-object-element)
-   [Objeto shell](#shell-object)
    -   [Seguridad](#security)
-   [Objetos de carpeta](#folder-objects)

## <a name="shell-versions"></a>Versiones del shell

Muchos de los objetos de Shell están disponibles [en la versión 4.71](versions.md) del shell. Otras están disponibles en la versión 5.00 y posteriores. La versión 5.00 pasó a estar disponible con Windows 2000. En la tabla siguiente se muestra cada objeto shell en la versión del shell en la que el objeto pasó a estar disponible.



| Versión 4.71                                            | Versión 5.00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Carpeta**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Carpeta2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Creación de instancias de objetos de shell

Para crear instancias de los objetos de Shell en Visual Basic aplicaciones con enlace temprano, agregue referencias a las siguientes bibliotecas en el proyecto:

-   Controles de Internet de Microsoft (SHDocVw)
-   Controles y automatización de Microsoft Shell (Shell32)

### <a name="late-binding"></a>Enlace en tiempo de tarde

También puede crear instancias de muchos de los objetos de Shell con enlace en tiempo de tarde. Este enfoque funciona en Visual Basic y en script. En el ejemplo siguiente se muestra cómo crear una instancia del [**objeto Shell**](shell.md) en JScript.


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



En el ejemplo siguiente se muestra cómo crear una instancia del [**objeto Folder**](folder.md) en VBScript.


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



En el ejemplo anterior, *sDir es* la ruta de acceso al [**objeto Folder.**](folder.md) Tenga en cuenta [**que los valores de enumeración ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) no están disponibles en el script.

El ProgID de cada uno de los objetos de Shell se muestra en la tabla siguiente.



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft.DiskQuota.1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | No se puede enlazar en tiempo de tarde                                                                        |
| [**Carpeta**](folder.md)                                | Cáscara. Shell \_ Application.NameSpace("...")                                               |
| [**Carpeta2**](folder2-object.md)                       | Cáscara. Shell \_ Application.NameSpace("...")                                               |
| [**FolderItem**](folderitem.md)                        | Cáscara. Shell \_ Application.NameSpace("..."). Self o Folder.Items.Item o Folder.ParseName |
| [**FolderItems**](folderitems.md)                      | Folder.Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Folder.Items                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell.NameSpace("..."). Self.Verbs.Item()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem.Verbs o Shell.NameSpace("..."). Self.Verbs                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | Cáscara. Aplicación de \_ shell                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink           |
| [**Shell**](shell.md)                                  | Cáscara. Aplicación de \_ shell                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell.NameSpace("..."). Self o Shell.NameSpace("..."). Items()                           |
| [**ShellFolderView**](shellfolderview.md)              | No se puede enlazar en tiempo de tarde                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | No se puede enlazar en tiempo de tarde                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell.NameSpace("..."). Self.GetLink o Shell.NameSpace("..."). Items(). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | No se puede enlazar en tiempo de tarde                                                                        |
| [**ShellWindows**](shellwindows.md)                    | Cáscara. Shell \_ Windows o ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | No se puede enlazar en tiempo de tarde                                                                        |



 

### <a name="html-object-element"></a>Elemento HTML OBJECT

También puede usar el elemento [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para crear instancias de objetos de Shell en una página HTML. Para ello, establezca el atributo  ID del elemento **OBJECT** en el nombre de variable que usará en los scripts e identifique el objeto con su número registrado (CLASSID). El siguiente código HTML crea una instancia del [**objeto ShellFolderItem**](shellfolderitem-object.md) mediante el **elemento OBJECT.**


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



En la tabla siguiente se muestra cada objeto de Shell y su CLASSID correspondiente.



| Objeto shell                                           | CLASSID                              |
|--------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Carpeta**](folder.md)                                | QUEBDE60-C3FF-11CE-8350-444553540000 |
| [**Carpeta2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
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



 

## <a name="shell-object"></a>Objeto shell

El [**objeto Shell**](shell.md) representa los objetos del Shell. Puede usar los métodos expuestos por el objeto shell para:

-   Abra, explore y busque carpetas.
-   Minimice, restaure, en cascada o abra ventanas de mosaico.
-   Inicie Panel de control aplicaciones.
-   Mostrar cuadros de diálogo del sistema.

Los usuarios quizás estén más familiarizados con los comandos a los que acceden desde el **menú** Inicio y el menú contextual de la barra de tareas. El menú contextual de la barra de tareas aparece cuando los usuarios hacen clic con el botón derecho en la barra de tareas. La siguiente aplicación HTML (HTA) genera una página de [](shell.md) inicio con botones que implementan muchos de los métodos del objeto shell. Algunos de estos métodos implementan características en el **menú** Inicio y en el menú contextual de la barra de tareas.


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

Como aplicación, un HTA se ejecuta con un modelo de seguridad diferente al de una página web. Para interactuar con una página web que implementa la funcionalidad de los objetos de Shell, los usuarios deben habilitar los controles Initialize y **script ActiveX no** marcados como seguros para la zona de seguridad en la que están viendo la página.

## <a name="folder-objects"></a>Objetos de carpeta

El [**objeto Folder**](folder.md) representa una carpeta shell. Puede usar los métodos expuestos por el objeto Folder para:

-   Obtenga información sobre una carpeta.
-   Cree subcarpetas.
-   Copie y mueva objetos de archivo a la carpeta .

El [**objeto FolderItem**](folderitem.md) representa un elemento de una carpeta de Shell. Sus propiedades permiten recuperar información sobre el elemento. Puede usar los métodos expuestos por este objeto para ejecutar los verbos de un elemento o para recuperar información sobre el objeto [**FolderItemVerbs**](folderitemverbs.md) de un elemento.

El [**objeto FolderItems**](folderitems.md) representa una colección de elementos de una carpeta de Shell. Sus métodos y propiedades permiten recuperar información sobre la colección.

En el Visual Basic siguiente se muestra la relación entre varios de los objetos de carpeta y cómo se pueden usar juntos. Cuando el usuario hace clic en el botón de comando denominado **cmdGetPath**, el programa muestra un cuadro de diálogo que permite al usuario seleccionar una carpeta de **Mi PC**, donde ssfDRIVES es el valor de enumeración [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) **para Mi PC**. Cuando el usuario elige una carpeta, la ruta de acceso de la carpeta se muestra en el cuadro de texto denominado **txtPath**.


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



En el ejemplo JScript siguiente, que es una traducción directa del ejemplo de VBScript anterior, observe cómo se usan los paréntesis vacíos '()' para invocar los métodos [**Items**](folder-items.md) y [**Item.**](folderitems-item.md)


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



 

 
