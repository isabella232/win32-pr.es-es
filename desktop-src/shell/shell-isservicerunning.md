---
description: Devuelve un valor que indica si se está ejecutando un servicio determinado.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Método Shell. IsServiceRunning (Shldisp. h)
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
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909881"
---
# <a name="shellisservicerunning-method"></a>Shell. IsServiceRunning (método)

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

*sServiceName* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene el nombre del servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **variante \** _

Devuelve _ *true** si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **variante \** _

Devuelve _ *true** si se está ejecutando el servicio especificado por *sServiceName* ; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **IsServiceRunning** para determinar si el servicio themes se está ejecutando para una aplicación. Se muestra el uso de JScript y VBScript.

JScript.net


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



VBScript


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
