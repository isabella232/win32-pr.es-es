---
description: Actualiza el contenido del menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Método Shell. RefreshMenu (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985543"
---
# <a name="shellrefreshmenu-method"></a>Shell. RefreshMenu (método)

Actualiza el contenido del menú **Inicio** . Solo se usa con sistemas anteriores a Windows XP.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

La funcionalidad que proporciona **RefreshMenu** se administra automáticamente en Windows XP o posterior. No llame a este método en ese sistema operativo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra **RefreshMenu** en uso. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

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



 

 




