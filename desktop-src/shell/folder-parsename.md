---
description: Crea y devuelve un objeto carpeta que representa un elemento especificado.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Método Folder. ParseName (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808030"
---
# <a name="folderparsename-method"></a>Folder. ParseName (método)

Crea y devuelve un objeto [**carpeta**](folderitem.md) que representa un elemento especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bName* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena que especifica el nombre del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **carpeta**](folderitem.md)\*\***

Una referencia de objeto al objeto [**carpeta**](folderitem.md) .

## <a name="remarks"></a>Observaciones

**ParseName** no debe usarse para carpetas virtuales como mis documentos.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **ParseName** para crear un objeto que representa el elemento de carpeta Clock.avi en la carpeta C: \\ Windows. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
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



 

 
