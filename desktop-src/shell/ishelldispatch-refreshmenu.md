---
description: Obtenga información sobre el método IShellDispatch.RefreshMenu, que actualiza el contenido de la menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Método IShellDispatch.RefreshMenu (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404678"
---
# <a name="ishelldispatchrefreshmenu-method"></a>Método IShellDispatch.RefreshMenu

Actualiza el contenido del **menú** Inicio. Solo se usa con sistemas anteriores a Windows XP.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método se implementa y se accede a través del [**método Shell.TrayProperties.**](shell-trayproperties.md)

La funcionalidad **que proporciona RefreshMenu** se controla automáticamente en Windows XP o versiones posteriores. No llame a este método en Windows XP o versiones posteriores.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de RefreshMenu** en JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

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



 

 




