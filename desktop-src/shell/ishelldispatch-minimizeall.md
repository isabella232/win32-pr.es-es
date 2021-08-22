---
description: Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Minimizar todos los Windows en sistemas anteriores o hacer clic en el icono Mostrar escritorio de la barra de tareas.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Método IShellDispatch.MinimizeAll (Shldisp.h)
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
ms.openlocfilehash: 18f1256f93c9cd18d0c904f090716641b466e91319dbef323ee5107b802f82ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452990"
---
# <a name="ishelldispatchminimizeall-method"></a>Método IShellDispatch.MinimizeAll

Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en  la barra de tareas y seleccionar Minimizar todos **los Windows** en sistemas anteriores o hacer clic en el icono Mostrar escritorio de la barra de tareas.

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

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.MinimizeAll.**](shell-minimizeall.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **MinimizeAll** en uso para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



Vbscript:


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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




