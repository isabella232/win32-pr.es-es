---
description: 'Método IShellDispatch2.GetSystemInformation: recupera información del sistema.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Método IShellDispatch2.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e99aa3e88a13327d7de133b8207ee9626db23a4cbbef9c9ffcaca5582d8e10d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111515"
---
# <a name="ishelldispatch2getsysteminformation-method"></a>Método IShellDispatch2.GetSystemInformation

Recupera información del sistema.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** especifica la información del sistema que se solicita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **Variant**

Devuelve el valor de la información solicitada del sistema. El tipo de valor devuelto depende de la información del sistema que se solicite. Para obtener información detallada, consulte la sección Comentarios.

### <a name="vb"></a>VB

Tipo: **Variant**

Devuelve el valor de la información solicitada del sistema. El tipo de valor devuelto depende de la información del sistema que se solicite. Para obtener información detallada, consulte la sección Comentarios.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.GetSystemInformation.**](./shell-getsysteminformation.md)

Este método se puede usar para solicitar muchos valores de información del sistema. En la tabla siguiente se proporciona *el valor sName* que se usa para solicitar la información y el tipo asociado del valor devuelto.



*sName*

Tipo de valor devuelto

Descripción

DirectoryServiceAvailable

**Boolean**

Establezca en **true** si el servicio de directorio está disponible; de lo contrario, **false**.

DoubleClickTime

**Entero**

Hora de doble clic, en milisegundos.

ProcessorLevel

**Entero**

**Windows Vista y versiones posteriores.** Nivel de procesador. Devuelve 3, 4 o 5 para procesadores de nivel x386, x486 y Pentium, respectivamente.

ProcessorSpeed

**Entero**

Velocidad del procesador, en megahercios (MHz).

ProcessorArchitecture

**Entero**

Arquitectura del procesador. Para más información, consulte la explicación del **miembro wProcessorArchitecture** de la [**estructura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

PhysicalMemoryInstalled

**Entero**

Cantidad de memoria física instalada, en bytes.

Los siguientes son válidos solo en Windows XP.

IsOS \_ Professional

**Boolean**

Se establece **en true** si el sistema operativo está Windows XP Professional Edition; de lo contrario, **false**.

IsOS \_ Personal

**Boolean**

Se establece **en true** si el sistema operativo está Windows XP Home Edition; de lo contrario, **false**.

Lo siguiente solo es válido en Windows XP y versiones posteriores.

DomainMember de IsOS \_

**Boolean**

Establezca en **true** si el equipo es miembro de un dominio; de lo contrario, **false**.



 

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **GetSystemInformation** para JScript y VBScript.

JScript:


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
