---
description: 'Método Shell.NameSpace: crea y devuelve un objeto Folder para la carpeta especificada.'
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Método Shell.NameSpace (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 41542f133961104180257b9c15b1843f3458bf6d9d2dd156fa3d97ea7b9ca87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857744"
---
# <a name="shellnamespace-method"></a>Método Shell.NameSpace

Crea y devuelve un [**objeto Folder**](folder.md) para la carpeta especificada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*vDir* \[ En\]
</dt> <dd>

Tipo: **Variant**

Carpeta para la que se va a crear el [**objeto Folder.**](folder.md) Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript ni JScript. En esos casos, los valores numéricos deben usarse en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **[ **Carpeta**](folder.md)\*\***

Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null.**

### <a name="vb"></a>VB

Tipo: **[ **Carpeta**](folder.md)\*\***

Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra NameSpace** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
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



 

 




