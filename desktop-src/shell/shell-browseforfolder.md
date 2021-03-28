---
description: Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de carpeta de la carpeta seleccionada.
title: Método Shell. BrowseForFolder (Shldisp. h)
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
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082894"
---
# <a name="shellbrowseforfolder-method"></a>Shell. BrowseForFolder (método)

Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de [**carpeta**](folder.md) de la carpeta seleccionada.

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

*HWnd* \[ de\]
</dt> <dd>

Tipo: **Integer**

Identificador de la ventana primaria del cuadro de diálogo. Este valor puede ser cero.

</dd> <dt>

*sTitle* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valor de **cadena** que representa el título que se muestra en el cuadro de diálogo **examinar** .

</dd> <dt>

*iOptions* \[ de\]
</dt> <dd>

Tipo: **Integer**

Valor **entero** que contiene las opciones para el método. Puede ser cero o una combinación de los valores enumerados en el miembro **ulFlags** de la estructura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .

</dd> <dt>

*vRootFolder* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Carpeta raíz que se va a utilizar en el cuadro de diálogo. El usuario no puede examinar más arriba en el árbol que esta carpeta. Si no se especifica este valor, la carpeta raíz usada en el cuadro de diálogo es el escritorio. Este valor puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript. En estos casos, se deben usar los valores numéricos en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **carpeta \* \***

Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta seleccionada.

### <a name="vb"></a>VB

Tipo: **carpeta \* \***

Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta seleccionada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **BrowseForFolder** para mostrar una ventana de exploración titulada "example" con la raíz de la carpeta Windows. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


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



VBScript


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
