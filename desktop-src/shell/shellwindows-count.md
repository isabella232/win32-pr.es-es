---
description: 'Propiedad ShellWindows.Count: contiene el número de elementos de la colección.'
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Propiedad ShellWindows.Count (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103943"
---
# <a name="shellwindowscount-property"></a>Propiedad ShellWindows.Count

Contiene el número de elementos de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a>Valor de propiedad

Entero **que** contiene un valor para la **propiedad Count.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra Count** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




