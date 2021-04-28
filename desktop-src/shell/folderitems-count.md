---
description: 'Propiedad FolderItems.Count: contiene el número de elementos de la colección.'
ms.assetid: 383382d5-7e3f-4b27-bebf-6b79dbe677b8
title: Propiedad FolderItems.Count (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a2bde6d938bde675c52c93f09916a70ba0e21f9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089613"
---
# <a name="folderitemscount-property"></a>Propiedad FolderItems.Count

Contiene el número de elementos de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iCount = FolderItems.Count
```



## <a name="property-value"></a>Valor de propiedad

Entero **que** contiene un valor para la **propiedad Count.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa Count** para recuperar el recuento de elementos de la carpeta de Windows. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnFolderItemsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var nCount;
                
                nCount = objFolderItems.Count;
                alert(nCount);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




