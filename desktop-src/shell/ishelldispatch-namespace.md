---
description: Crea y devuelve un objeto de carpeta para la carpeta especificada.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Método IShellDispatch. NameSpace (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543150"
---
# <a name="ishelldispatchnamespace-method"></a>IShellDispatch. NameSpace (método)

Crea y devuelve un objeto de [**carpeta**](folder.md) para la carpeta especificada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*vDir* \[ de\]
</dt> <dd>

Tipo: **variante**

Carpeta para la que se va a crear el objeto de [**carpeta**](folder.md) . Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript. En estos casos, se deben usar los valores numéricos en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **[ **carpeta**](folder.md)\*\***

Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null**.

### <a name="vb"></a>VB

Tipo: **[ **carpeta**](folder.md)\*\***

Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null**.

## <a name="remarks"></a>Observaciones

Este método se implementa y se obtiene acceso a él a través del método [**Shell. Namespace**](shell-namespace.md) .

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso del [**espacio de nombres**](shell-namespace.md) en JScript, VBScript y Visual Basic.

JScript.net


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



VBScript


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




