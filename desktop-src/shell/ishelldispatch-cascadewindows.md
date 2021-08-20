---
description: En cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Ventanas en cascada.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Método IShellDispatch.CascadeWindows (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7e14514c31f81327d9d0c0217479d2ce746c61ed58c9f71e1b2fa6f19f4e31ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032283"
---
# <a name="ishelldispatchcascadewindows-method"></a>Método IShellDispatch.CascadeWindows

En cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Ventanas en cascada**.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a este método a través [**del método Shell.CascadeWindows.**](shell-cascadewindows.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de CascadeWindows** en JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
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



 

 




