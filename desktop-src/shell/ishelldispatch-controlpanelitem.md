---
description: Ejecuta la aplicación Panel de control especificada.
title: Método IShellDispatch.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 89ea8431df7e8cac09a041bd9a16c805633cd3ec82a2cc506cb30fcf0f0cd39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032263"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a>Método IShellDispatch.ControlPanelItem

Ejecuta la aplicación Panel de control especificada. Si la aplicación ya está abierta, activará la instancia en ejecución.

> [!Note]  
> A Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función. Para abrir esas Panel de control, pase el nombre canónico a control.exe. Por ejemplo:
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDir* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

El Panel de control nombre de archivo de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.ControlPanelItem.**](shell-controlpanelitem.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se [**usa ControlPanelItem**](shell-controlpanelitem.md) para ejecutar el Panel de control **de** Propiedades de pantalla elemento. El uso se muestra para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
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



 

 
