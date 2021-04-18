---
description: Recupera información del sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Método Shell. GetSystemInformation (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985974"
---
# <a name="shellgetsysteminformation-method"></a>Shell. GetSystemInformation (método)

Recupera información del sistema.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que especifica la información del sistema que se solicita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **variante**

Devuelve el valor de la información del sistema solicitada. El tipo de valor devuelto depende de la información del sistema que se solicite. Para obtener información detallada, consulte la sección Comentarios.

### <a name="vb"></a>VB

Tipo: **variante**

Devuelve el valor de la información del sistema solicitada. El tipo de valor devuelto depende de la información del sistema que se solicite. Para obtener información detallada, consulte la sección Comentarios.

## <a name="remarks"></a>Observaciones

Este método se puede utilizar para solicitar muchos valores de información del sistema. En la tabla siguiente se proporciona el valor de *sName* que se usa para solicitar la información y el tipo asociado del valor devuelto.



*sName*

Tipo de valor devuelto

Descripción

DirectoryServiceAvailable

**Boolean**

Establézcalo en **true** si el servicio de directorio está disponible; en caso contrario, **false**.

DoubleClickTime

**Entero**

Tiempo de doble clic, en milisegundos.

ProcessorLevel

**Entero**

**Windows Vista y versiones posteriores**. Nivel de procesador. Devuelve 3, 4 o 5 para los procesadores x386, x486 y Pentium, respectivamente.

Velocidaddeprocesador

**Entero**

La velocidad del procesador, en megahercios (MHz).

ProcessorArchitecture

**Entero**

La arquitectura del procesador. Para obtener más información, consulte la descripción del miembro **wProcessorArchitecture** de la estructura de [**\_ información del sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

PhysicalMemoryInstalled

**Entero**

La cantidad de memoria física instalada, en bytes.

Lo siguiente solo es válido en Windows XP.

Archivos ISO \_ Professional

**Boolean**

Establézcalo en **true** si el sistema operativo es Windows XP Professional Edition; en caso contrario, **false**.

Personal de archivos ISO \_

**Boolean**

Establézcalo en **true** si el sistema operativo es Windows XP Home Edition; en caso contrario, **false**.

Lo siguiente solo es válido en Windows XP y versiones posteriores.

Archivos ISO \_ DomainMember

**Boolean**

Establézcalo en **true** si el equipo es miembro de un dominio; en caso contrario, **false**.



 

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **GetSystemInformation** para JScript y VBScript.

JScript.net


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



VBScript


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
