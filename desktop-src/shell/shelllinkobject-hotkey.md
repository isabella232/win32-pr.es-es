---
description: Obtiene o establece el método abreviado de teclado para el vínculo.
ms.assetid: edc65fe8-c7f3-46d0-86ca-1c0c93e7ca64
title: Propiedad ShellLinkObject. Hotkey (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Hotkey
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ab8615421eee7289e5f0bb58582bf8e0d48f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985958"
---
# <a name="shelllinkobjecthotkey-property"></a>Propiedad ShellLinkObject. Hotkey

Obtiene o establece el método abreviado de teclado para el vínculo.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
iHotkey = ShellLinkObject.Hotkey
ShellLinkObject.Hotkey(iHotkey) = iHotkey
```



## <a name="property-value"></a>Valor de propiedad

método abreviado de teclado del vínculo. El método abreviado de teclado virtual está en bytes de orden inferior, y los marcadores modificadores se encuentran en el byte de orden superior. Las marcas modificadoras pueden ser una combinación de los valores siguientes.

<dt>



 (1)


</dt> <dd>

Tecla Mayús

</dd> <dt>



 (2)


</dt> <dd>

Tecla CTRL

</dd> <dt>



 (4)


</dt> <dd>

tecla ALT

</dd> <dt>



 (8)


</dt> <dd>

Clave extendida

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellShellLinkObjectHotkeyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var nHotkey;
                    
                    // Get the keyboard shortcut for the ShellLinkObject.
                    nHotkey = objShellLink.Hotkey;
                    alert(nHotkey);
                    
                    // Set the keyboard shortcut for the ShellLinkObject.
                    objShellLink.Hotkey = 4;
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnShellLinkObjectHotkeyVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim nHotkey
                                
                                'Get the keyboard shortcut for the ShellLinkObject.
                                nHotkey = objShellLink.Hotkey
                                alert(nHotkey)
                                
                                'Set the keyboard shortcut for the ShellLinkObject.
                                objShellLink.Hotkey = 4
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function

 </script>
```



Visual Basic:


```VB
Private Sub fnShellLinkObjectHotkeyVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim nHotkey As Integer
                            
                            'Get the keyboard shortcut for the ShellLinkObject.
                            nHotkey = objShellLink.Hotkey
                            Debug.Print nHotkey
                            
                            'Set the keyboard shortcut for the ShellLinkObject.
                            objShellLink.Hotkey = 4
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 




