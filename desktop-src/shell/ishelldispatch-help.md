---
description: Muestra la Windows ayuda y soporte técnico. Este método tiene el mismo efecto que hacer clic en el menú Inicio y seleccionar Ayuda y soporte técnico.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Método IShellDispatch.Help (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 53b5476b89e4267415f1310d6e7cbf5507e953d643f61eec9ad8315febd56c41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111535"
---
# <a name="ishelldispatchhelp-method"></a>Método IShellDispatch.Help

Muestra la Windows ayuda y soporte técnico. Este método tiene el mismo efecto que hacer clic en **el menú** Inicio y seleccionar Ayuda y **soporte técnico.**

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.Help.**](shell-help.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **la Ayuda** en JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



Vbscript:


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

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



 

 




