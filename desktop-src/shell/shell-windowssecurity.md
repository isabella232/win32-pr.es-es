---
description: Muestra el cuadro de diálogo seguridad de Windows.
title: Método Shell. WindowsSecurity (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: bbefa4c772adde64b8142b7e3563315fe4833b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545907"
---
# <a name="shellwindowssecurity-method"></a>Shell. WindowsSecurity (método)

Muestra el cuadro de diálogo **seguridad de Windows** .

## <a name="syntax"></a>Sintaxis


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método muestra el cuadro de diálogo que se muestra después de presionar CTRL + ALT + SUPR o el uso de la opción seguridad en el menú **Inicio** .

> [!Note]  
> Este método solo se puede usar cuando está conectado mediante una sesión de terminal a Microsoft Terminal Server.

 

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **WindowsSecurity** para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6,0 o posterior)</dt> </dl> |



 

 




