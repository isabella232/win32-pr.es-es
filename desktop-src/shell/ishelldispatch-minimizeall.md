---
description: Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar minimizar todas las ventanas en sistemas antiguos o hacer clic en el icono Mostrar escritorio en la barra de tareas.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Método IShellDispatch. MinimizeAll (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543147"
---
# <a name="ishelldispatchminimizeall-method"></a>IShellDispatch. MinimizeAll, método

Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **minimizar todas las ventanas** en sistemas antiguos o hacer clic en el icono **Mostrar escritorio** en la barra de tareas.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método se implementa y se obtiene acceso a él a través del método [**Shell. MinimizeAll**](shell-minimizeall.md) .

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **MinimizeAll** en uso para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




