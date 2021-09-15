---
description: 'Método Shell.IsServiceRunning: devuelve un valor que indica si se está ejecutando un servicio determinado.'
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Método Shell.IsServiceRunning (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468104"
---
# <a name="shellisservicerunning-method"></a>Método Shell.IsServiceRunning

Devuelve un valor que indica si se está ejecutando un servicio determinado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
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

## <a name="remarks"></a>Observaciones

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **IsServiceRunning para** determinar si el servicio Themes se está ejecutando para una aplicación. El uso se muestra para JScript y VBScript.

JScript:


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



Vbscript:


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
