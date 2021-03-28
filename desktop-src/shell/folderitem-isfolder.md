---
description: Indica si el elemento es una carpeta.
ms.assetid: fb080c8f-04b1-4f9a-9219-0951a2e950ea
title: Propiedad carpeta. IsFolder (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bf0bd4eb9b7964620fe705d6e8f4d10644ca234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984187"
---
# <a name="folderitemisfolder-property"></a>Propiedad carpeta. IsFolder

Indica si el elemento es una carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
bIsFolder = FolderItem.IsFolder
```



## <a name="property-value"></a>Valor de propiedad

Un **valor booleano** que recibe **true** si el elemento es una carpeta o **false** en caso contrario.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **IsFolder** para determinar si el directorio de Windows es una carpeta. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnIsFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFolder;
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFolder
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIsFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFolder
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




