---
description: Recupera el objeto FolderItemVerbs del elemento. Este objeto es la colección de verbos que se pueden ejecutar en el elemento.
ms.assetid: e31160cd-093a-45a6-a066-58120c44eb2c
title: Método carpeta. Verbs (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f15c2471f749748f7928a45aa03037d955c75d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153608"
---
# <a name="folderitemverbs-method"></a>Carpeta. Verbs (método)

Recupera el objeto [**FolderItemVerbs**](folderitemverbs.md) del elemento. Este objeto es la colección de verbos que se pueden ejecutar en el elemento.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = FolderItem.Verbs()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FolderItemVerbs**](folderitemverbs.md)\*\***

Una referencia de objeto al objeto [**FolderItemVerbs**](folderitemverbs.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se utilizan **verbos** para recuperar el objeto [**FolderItemVerbs**](folderitemverbs.md) que representa el conjunto de verbos que se pueden ejecutar en la carpeta Windows. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnFolderItemVerbsJ()
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
                var objItemVerbs;
                
                objItemVerbs = objFolderItem.Verbs();
                if (objItemVerbs != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemVerbsVB()
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
                    dim objItemVerbs
                    
                    set objItemVerbs = objFolderItem.Verbs
                        if (not objItemVerbs is nothing) then
                            'Add code here
                        end if
                    set objItemVerbs = nothing
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
Private Sub fnFolderItemVerbsVB()
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
                    Dim objItemVerbs As FolderItemVerbs
                    
                    Set objItemVerbs = objFolderItem.Verbs
                        If (Not objItemVerbs Is Nothing) Then
                            'Add code here
                        End If
                    Set objItemVerbs = Nothing
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Carpeta**](folderitem.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> <dt>

[**DoIt**](folderitemverb-doit.md)
</dt> </dl>

 

 




