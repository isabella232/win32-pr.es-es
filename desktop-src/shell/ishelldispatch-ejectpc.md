---
description: 'Método IShellDispatch.EjectPC: expulsa el equipo de su estación de acoplamiento. Esto es lo mismo que hacer clic en menú Inicio y seleccionar Expulsar PC, si el equipo admite este comando.'
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Método IShellDispatch.EjectPC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086643"
---
# <a name="ishelldispatchejectpc-method"></a>Método IShellDispatch.EjectPC

Expulsa el equipo de su estación de acoplamiento. Esto es lo mismo que hacer clic en el **menú** Inicio y seleccionar **Expulsar PC** si el equipo admite este comando.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.EjectPC.**](shell-ejectpc.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de EjectPC** en JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




