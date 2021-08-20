---
description: Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Mostrar ventanas apiladas.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Método IShellDispatch.TileHorizontally (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e83870abcec849b9e8bf5a2583b6e25d4e2a2280ead4df9c4979014149a643ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678449"
---
# <a name="ishelldispatchtilehorizontally-method"></a>Método IShellDispatch.TileHorizontally

Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Mostrar ventanas apiladas.**

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.TileHorizontally.**](shell-tilehorizontally.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso **de TileHorizontally** en JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

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



 

 




