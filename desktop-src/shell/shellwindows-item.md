---
description: Recupera un objeto InternetExplorer que representa la ventana shell.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Método ShellWindows.Item (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468038"
---
# <a name="shellwindowsitem-method"></a>Método ShellWindows.Item

Recupera un objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana shell.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iIndex* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Índice de base cero del elemento que se va a recuperar. Este valor debe ser menor que el valor de la [**propiedad Count.**](shellwindows-count.md) Si se omite este valor, se usa un valor predeterminado de 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Referencia de objeto al [**objeto InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana shell.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se [**usa Item**](folderitemverbs-item.md) para recuperar el [**objeto InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa el primer elemento de ventana de Shell. Se muestra el uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
