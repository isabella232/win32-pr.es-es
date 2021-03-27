---
description: Obtiene el valor de una directiva especificada de Windows Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Método IShellDispatch4. ExplorerPolicy (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908233"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>IShellDispatch4. ExplorerPolicy, método

Obtiene el valor de una directiva especificada de Windows Internet Explorer.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPolicyName* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que especifica el nombre de la Directiva.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **variante \** _

Valor asociado al nombre de la Directiva especificada.

### <a name="vb"></a>VB

Tipo: _*variante \**_

Valor asociado al nombre de la Directiva especificada.

## <a name="remarks"></a>Observaciones

Los administradores de red pueden controlar y administrar el entorno informático de sus usuarios mediante la configuración de directivas.

El nombre de valor especificado debe estar dentro de la subclave _ *HKEY \_ Current \_ User **\\** software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer**. Si el nombre del valor no existe, el método devuelve **null**.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso correcto de **ExplorerPolicy** para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
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



 

 
