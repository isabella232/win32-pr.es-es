---
description: Inicia un servicio con nombre.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Método Shell. ServiceStart (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909878"
---
# <a name="shellservicestart-method"></a>Shell. ServiceStart (método)

Inicia un servicio con nombre.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceName* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene el nombre del servicio.

</dd> <dt>

*vPersistent* \[ de\]
</dt> <dd>

Tipo: **variante**

Establézcalo en **true** para que el servicio se inicie automáticamente por el administrador de control de servicios durante el inicio del sistema. Establézcalo en **false** para dejar la configuración del servicio sin cambios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **variante \** _

Devuelve _ *true** si es correcto; en caso contrario, **false**.

### <a name="vb"></a>VB

Tipo: **variante \** _

Devuelve _ *true** si es correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

El método devuelve **false** si el servicio ya se ha iniciado. Antes de llamar a este método, puede llamar a [**Shell. IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **ServiceStart** para iniciar el servicio Messenger. Se muestra el uso de JScript y VBScript.

JScript.net


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



VBScript


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
