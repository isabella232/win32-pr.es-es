---
description: 'Método IShellDispatch.NameSpace: crea y devuelve un objeto Folder para la carpeta especificada.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Método IShellDispatch.NameSpace (Shldisp.h)
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
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361055"
---
# <a name="ishelldispatchnamespace-method"></a>Método IShellDispatch.NameSpace

Crea y devuelve un [**objeto Folder**](folder.md) para la carpeta especificada.

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

*vDir* \[ En\]
</dt> <dd>

Tipo: **Variant**

Carpeta para la que se va a crear el [**objeto Folder.**](folder.md) Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript. En esos casos, los valores numéricos deben usarse en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **[ **Carpeta**](folder.md)\*\***

Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null.**

### <a name="vb"></a>VB

Tipo: **[ **Carpeta**](folder.md)\*\***

Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada. Si la carpeta no se ha creado correctamente, este valor devuelve **null.**

## <a name="remarks"></a>Observaciones

Este método se implementa y se accede a través del [**método Shell.NameSpace.**](shell-namespace.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de [**NameSpace**](shell-namespace.md) en JScript, VBScript y Visual Basic.

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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




