---
description: 'Método Shell.ShutdownWindows: muestra el cuadro de diálogo Cerrar Windows cierre. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar Apagar.'
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Método Shell.ShutdownWindows (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1e9149e42710541ef82d02ba4d55f1d9519741e078e06c60ab0d47c1209fa19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857734"
---
# <a name="shellshutdownwindows-method"></a>Método Shell.ShutdownWindows

Muestra el **cuadro de diálogo Windows** apagado. Esto es lo mismo que hacer clic en **el menú** Inicio y seleccionar **Apagar.**

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **muestra ShutdownWindows** en uso. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



Visual Basic:


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

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



 

 




