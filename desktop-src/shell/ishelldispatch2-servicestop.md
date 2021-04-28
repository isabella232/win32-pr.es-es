---
description: 'Método IShellDispatch2.ServiceStop: detiene un servicio con nombre.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Método IShellDispatch2.ServiceStop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117033"
---
# <a name="ishelldispatch2servicestop-method"></a>Método IShellDispatch2.ServiceStop

Detiene un servicio con nombre.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre del servicio.

</dd> <dt>

*vPersistent* \[ En\]
</dt> <dd>

Tipo: **Variant**

Establezca en **true para** que el administrador de control de servicios haya iniciado el servicio cuando se llame a [**ServiceStart.**](ishelldispatch2-servicestart.md) Para dejar la configuración del servicio sin cambios, establezca *vPersistent* en **false.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.ServiceStop.**](./shell-servicestop.md)

El método devuelve **false** si el servicio ya se ha detenido. Antes de llamar a este método, puede llamar a [**Shell.IsServiceRunning para**](./shell-isservicerunning.md) determinar el estado del servicio.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **ServiceStop para** detener el servicio Messenger. El uso se muestra para JScript y VBScript.

Jscript:


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

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



 

 
