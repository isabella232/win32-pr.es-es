---
description: Establece la ubicación del icono asignado al vínculo.
ms.assetid: 257bb8e2-29fa-4d2f-ac2d-3497cf12959c
title: Método ShellLinkObject. SetIconLocation (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.SetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 996f9648e9b9f59e1e84871abac1d6b37e2592d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997821"
---
# <a name="shelllinkobjectseticonlocation-method"></a>ShellLinkObject. SetIconLocation, método

Establece la ubicación del icono asignado al vínculo.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellLinkObject.SetIconLocation(
  sPath,
  iIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Spath* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ruta de acceso completa del archivo que contiene el icono.

</dd> <dt>

*iIndex* \[ de\]
</dt> <dd>

Tipo: **Integer**

Índice del icono del archivo especificado por *Spath*.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellLinkObjectSetIconLocationJ()
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
                    objShellLink.SetIconLocation(objShellLink.Path, 1);
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
    function fnShellLinkObjectSetIconLocationVB()
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
                                objShellLink.SetIconLocation objShellLink.Path, 1
                                objShellLink.Save
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
Private Sub fnShellLinkObjectSetIconLocationVB()
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
                            objShellLink.SetIconLocation objShellLink.Path, 1
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



 

 
