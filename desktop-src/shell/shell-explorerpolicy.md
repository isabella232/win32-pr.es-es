---
description: 'Método Shell.ExplorerPolicy: obtiene el valor de una directiva de Internet Explorer Windows especificada.'
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Método Shell.ExplorerPolicy (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 765e1dc46edbe5a27292c5d8ff940e29b269f8dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083703"
---
# <a name="shellexplorerpolicy-method"></a>Método Shell.ExplorerPolicy

Obtiene el valor de una directiva de windows Internet Explorer especificada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
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

El nombre de valor especificado debe estar dentro de la subclave **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer.** Si el nombre del valor no existe, el método devuelve **null**.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso adecuado de **ExplorerPolicy** para JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
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
            vReturn = objShell.ExplorerPolicy("ValueName")
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
        vReturn = objShell.ExplorerPolicy("ValueName")
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



 

 
