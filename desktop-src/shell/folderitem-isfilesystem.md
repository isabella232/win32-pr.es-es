---
description: Indica si el elemento forma parte del sistema de archivos.
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: Propiedad FolderItem.IsFileSystem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b618821880a713e3e76e3ae9c78454bb15469a578ab4d40def1a66d2d763c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860215"
---
# <a name="folderitemisfilesystem-property"></a>Propiedad FolderItem.IsFileSystem

Indica si el elemento forma parte del sistema de archivos.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a>Valor de propiedad

Valor **booleano** que recibe **true** si el elemento forma parte del sistema de archivos o **false** si no es así.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa IsFileSystem** para determinar si Windows carpeta forma parte del sistema de archivos. Se muestra el uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
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
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
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
                                
                    bReturn = objFolderItem.IsFileSystem
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
Private Sub fnIsFileSystemVB()
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
                    
                    bReturn = objFolderItem.IsFileSystem
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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




