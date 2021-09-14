---
description: Obtiene un objeto que representa el elemento primario del objeto actual.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Propiedad Shell.Parent (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361031"
---
# <a name="shellparent-property"></a>Propiedad Shell.Parent

Obtiene un objeto que representa el elemento primario del objeto actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto primario.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de **Parent** JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
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



 

 
