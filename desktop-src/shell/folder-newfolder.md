---
description: Crea una nueva carpeta.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Método Folder.NewFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574556"
---
# <a name="foldernewfolder-method"></a>Método Folder.NewFolder

Crea una nueva carpeta.

## <a name="syntax"></a>Sintaxis


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bName* 
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena que especifica el nombre de la nueva carpeta.

</dd> <dt>

*vOptions* \[ Opcional\]
</dt> <dd>

Tipo: **Variant**

Este valor no se utiliza actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS). Si intenta llamar a un método sin implementar, se 0x800A01BD error (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa NewFolder** para crear la nueva carpeta C: \\ TestFolder. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
