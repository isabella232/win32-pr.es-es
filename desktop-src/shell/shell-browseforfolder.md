---
description: 'Método Shell.BrowseForFolder: crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de la carpeta seleccionada.'
title: Método Shell.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 26677173cce2b72d1a0ba6bdc941cd2407908712
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247989"
---
# <a name="shellbrowseforfolder-method"></a>Método Shell.BrowseForFolder

Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de [**la carpeta**](folder.md) seleccionada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* \[ En\]
</dt> <dd>

Tipo: **Entero**

Identificador de la ventana primaria del cuadro de diálogo. Este valor puede ser cero.

</dd> <dt>

*sTitle* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor **string** que representa el título que se muestra dentro del **cuadro de** diálogo Examinar.

</dd> <dt>

*iOptions* \[ En\]
</dt> <dd>

Tipo: **Entero**

Valor **Entero** que contiene las opciones para el método . Puede ser cero o una combinación de los valores enumerados en el **miembro ulFlags** de la [**estructura BROWSEINFO.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)

</dd> <dt>

*vRootFolder* \[ in, opcional\]
</dt> <dd>

Tipo: **Variant**

Carpeta raíz que se usará en el cuadro de diálogo. El usuario no puede examinar más arriba en el árbol que esta carpeta. Si no se especifica este valor, la carpeta raíz que se usa en el cuadro de diálogo es el escritorio. Este valor puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript. En esos casos, los valores numéricos deben usarse en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* \* FOLDER**

Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.

### <a name="vb"></a>VB

Tipo: **\* \* FOLDER**

Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa BrowseForFolder para** mostrar una ventana de exploración titulada "Example" rooteado en Windows carpeta. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
