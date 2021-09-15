---
description: 'Método IShellDispatch2.CanStartStopService: determina si el usuario actual puede iniciar y detener el servicio con nombre.'
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Método IShellDispatch2.CanStartStopService (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248072"
---
# <a name="ishelldispatch2canstartstopservice-method"></a>Método IShellDispatch2.CanStartStopService

Determina si el usuario actual puede iniciar y detener el servicio con nombre.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceName* \[ En\]
</dt> <dd>

Tipo: **Cadena**

Cadena **que** contiene el nombre del servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Devuelve **true** si el usuario puede iniciar y detener el servicio; de lo contrario, **false**.

## <a name="remarks"></a>Observaciones

Este método se implementa y se accede a través del [**método Shell.CanStartStopService.**](./shell-canstartstopservice.md)

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el **uso de CanStartStopService** para JScript y VBScript.

JScript:


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
