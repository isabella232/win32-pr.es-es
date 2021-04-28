---
description: 'Método IShellDispatch2.IsServiceRunning: devuelve un valor que indica si se está ejecutando un servicio determinado.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Método IShellDispatch2.IsServiceRunning (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117093"
---
# <a name="ishelldispatch2isservicerunning-method"></a>Método IShellDispatch2.IsServiceRunning

Devuelve un valor que indica si se está ejecutando un servicio determinado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre del servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Devuelve **true** si se está ejecutando el servicio especificado *por sServiceName;* de lo contrario, **false**.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.IsServiceRunning.**](./shell-isservicerunning.md)

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **IsServiceRunning para** determinar si el servicio Themes se está ejecutando para una aplicación. El uso se muestra para JScript y VBScript.

Jscript:


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
