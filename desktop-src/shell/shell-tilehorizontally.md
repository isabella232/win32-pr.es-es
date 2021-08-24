---
description: Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Icono Windows horizontalmente.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Método Shell.TileHorizontally (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da11496ca9993c87f78a9209a2c6d04bc0167349a6c0b955a3b2823335f30464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709485"
---
# <a name="shelltilehorizontally-method"></a>Método Shell.TileHorizontally

Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Icono Windows horizontalmente.**

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra TileHorizontally** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




