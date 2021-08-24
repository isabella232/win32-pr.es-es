---
description: 'Método Shell.WindowsSecurity: muestra el Seguridad de Windows de diálogo.'
title: Método Shell.WindowsSecurity (Shldisp.h)
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
ms.openlocfilehash: 327855763220fd2ea1c2e0e6b93538c16fa27cf35cd65cba06888879580259c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592005"
---
# <a name="shellwindowssecurity-method"></a>Shell.WindowsSecurity (método)

Muestra el **cuadro Seguridad de Windows** de diálogo.

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

## <a name="remarks"></a>Comentarios

Este método muestra el cuadro de diálogo que se muestra después de presionar CTRL+ALT+SUPR o usar la opción de seguridad en el **menú** Inicio.

> [!Note]  
> Este método solo se puede usar cuando se conecta mediante una sesión de terminal a Microsoft Terminal Server.

 

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **WindowsSecurity** para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



Vbscript:


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



 

 




