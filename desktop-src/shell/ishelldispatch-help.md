---
description: Muestra la ventana de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú Inicio y seleccionar ayuda y soporte técnico.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Método IShellDispatch. Help (Shldisp. h)
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
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984710"
---
# <a name="ishelldispatchhelp-method"></a>IShellDispatch. Help (método)

Muestra la ventana de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú **Inicio** y seleccionar **ayuda y soporte técnico**.

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

## <a name="remarks"></a>Observaciones

Este método se implementa y se obtiene acceso a él a través del método [**Shell. Help**](shell-help.md) .

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de la **ayuda** en JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



VBScript


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




