---
description: Guarda todos los cambios realizados en el vínculo.
ms.assetid: 4c776c82-8eca-4c9b-9487-4a835affd2d8
title: Método ShellLinkObject. Save (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Save
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0283b839069464a1a059bd11ef52b522f7ec7072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997940"
---
# <a name="shelllinkobjectsave-method"></a>ShellLinkObject. Save (método)

Guarda todos los cambios realizados en el vínculo.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellLinkObject.Save(
  [ sFile ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sFile* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Valor de cadena que contiene la ruta de acceso completa del archivo donde se va a guardar la nueva información del vínculo. Si no se especifica ningún archivo, se utiliza el archivo actual.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellLinkObjectSaveJ()
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
                    // Making a change to the ShellLinkObject.
                    objShellLink.Description = "New Description";
                    
                    // Saving the changes.
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectSaveVB()
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
                                'Making a change to the ShellLinkObject.
                                objShellLink.Description = "New Description"
                                
                                'Saving the changes.
                                objShellLink.Save()
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
Private Sub fnShellLinkObjectSaveVB()
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
                            'Making a change to the ShellLinkObject.
                            objShellLink.Description = "New Description"
                            'Saving the changes
                            objShellLink.Save
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



 

 




