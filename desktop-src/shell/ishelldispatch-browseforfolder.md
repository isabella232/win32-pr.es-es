---
description: 'Método IShellDispatch.BrowseForFolder: crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de la carpeta seleccionada.'
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Método IShellDispatch.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e70fd50d4b08787326f93cddf7ec55a0eaacb25fa815cc2b4c8246c1934494a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551835"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>Método IShellDispatch.BrowseForFolder

Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de [**la carpeta**](folder.md) seleccionada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
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

Carpeta raíz que se usará en el cuadro de diálogo. El usuario no puede examinar más arriba en el árbol que esta carpeta. Si no se especifica este valor, la carpeta raíz que se usa en el cuadro de diálogo es el escritorio. Este valor puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript ni JScript. En esos casos, los valores numéricos deben usarse en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* \* FOLDER**

Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.

### <a name="vb"></a>VB

Tipo: **\* \* FOLDER**

Referencia de objeto al objeto Folder de [**la carpeta**](folder.md) seleccionada.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.BrowseForFolder.**](shell-browseforfolder.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se **usa BrowseForFolder para** mostrar una ventana de exploración titulada "Ejemplo" con raíz en Windows carpeta. El uso se muestra para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
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
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
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



 

 
