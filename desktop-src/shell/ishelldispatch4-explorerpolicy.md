---
description: 'Método IShellDispatch4.ExplorerPolicy: obtiene el valor de una directiva de windows Internet Explorer especificada.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Método IShellDispatch4.ExplorerPolicy (Shldisp.h)
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
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116835"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>Método IShellDispatch4.ExplorerPolicy

Obtiene el valor de una directiva de Internet Explorer Windows especificada.

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

*bstrPolicyName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** especifica el nombre de la directiva.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Valor asociado al nombre de directiva especificado.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Valor asociado al nombre de directiva especificado.

## <a name="remarks"></a>Comentarios

Los administradores de red pueden controlar y administrar el entorno informático de sus usuarios estableciendo directivas.

El nombre del valor especificado debe estar dentro de la subclave **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer.** Si el nombre del valor no existe, el método devuelve **null.**

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso adecuado de **ExplorerPolicy** para JScript, VBScript y Visual Basic.

Jscript:


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



Vbscript:


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



 

 
