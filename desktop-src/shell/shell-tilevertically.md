---
description: Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar ventanas de mosaico verticalmente.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Método Shell. TileVertically (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985963"
---
# <a name="shelltilevertically-method"></a>Shell. TileVertically (método)

Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **ventanas de mosaico verticalmente**.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra **TileVertically** en uso. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

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



 

 




