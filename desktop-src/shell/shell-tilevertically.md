---
description: Iconos de todas las ventanas en el escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Icono Windows verticalmente.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Método Shell.TileVertically (Shldisp.h)
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
ms.openlocfilehash: add315a9e5656279a6a16ab5a3a9adc46ec91ab7eef3b5ec835fda242ec5b706
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090135"
---
# <a name="shelltilevertically-method"></a>Método Shell.TileVertically

Iconos de todas las ventanas en el escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Icono Windows verticalmente.**

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

En el ejemplo siguiente se **muestra TileVertically** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



Vbscript:


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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




