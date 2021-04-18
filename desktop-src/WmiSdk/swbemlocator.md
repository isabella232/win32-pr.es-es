---
description: Puede usar los métodos del objeto SWbemLocator para obtener un objeto SWbemServices que representa una conexión a un espacio de nombres en un equipo local o en un equipo host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objeto SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697250"
---
# <a name="swbemlocator-object"></a>Objeto SWbemLocator

Puede usar los métodos del objeto **SWbemLocator** para obtener un objeto [**SWbemServices**](swbemservices.md) que representa una conexión a un espacio de nombres en un equipo local o en un equipo host remoto. Después, puede usar los métodos del objeto **SWbemServices** para tener acceso a WMI. Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemLocator** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemLocator** tiene estos métodos.



| Método                                              | Descripción                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Se conecta a WMI en el equipo especificado.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemLocator** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso          | Descripción                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Seguridad\_**](swbemlocator-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="remarks"></a>Observaciones

En la parte superior del modelo de objetos de la biblioteca de scripting de WMI se encuentra el objeto SWbemLocator. SWbemLocator se utiliza para establecer una conexión autenticada con un espacio de nombres WMI, de forma muy similar a la función GetObject de VBScript y el moniker de WMI "winmgmts:" se usa para establecer una conexión autenticada con WMI. Sin embargo, SWbemLocator está diseñado para abordar dos escenarios de scripting específicos que no se pueden realizar mediante GetObject y el moniker de WMI. Debe usar SWbemLocator si necesita:

-   Proporcione las credenciales de usuario y contraseña para conectarse a WMI en un equipo remoto. El moniker de WMI utilizado con la función GetObject no incluye un mecanismo para especificar las credenciales. La mayoría de las actividades de WMI (incluidas todas las que se llevan a cabo en equipos remotos) requieren derechos de administrador. Si normalmente inicia sesión con una cuenta de usuario normal en lugar de una cuenta de administrador, no podrá realizar la mayoría de las tareas de WMI a menos que ejecute el script en credenciales alternativas.
-   Conéctese a WMI si está ejecutando un script de WMI desde una página web. No se puede usar la función GetObject al ejecutar scripts insertados en una página HTML porque Internet Explorer no permite el uso de GetObject por motivos de seguridad.

Además, es posible que desee usar SWbemLocator para conectarse a WMI si encuentra la cadena de conexión WMI que se usa con GetObject confuso o difícil.

Use CreateObject en lugar de GetObject para crear una referencia a SWbemLocator. Para crear la referencia, debe pasar la función CreateObject al identificador de programación de SWbemLocator (ProgID) "WbemScripting. SWbemLocator", como se muestra en la línea 2 del siguiente ejemplo de script. Después de obtener una referencia a un objeto SWbemLocator, llame al método ConnectServer para conectarse a WMI y obtener una referencia a un objeto SWbemServices. Esto se muestra en la línea 3 del script siguiente.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Para ejecutar un script en credenciales alternativas, incluya el nombre de usuario y la contraseña como parámetros adicionales que se pasan a ConnectServer. Por ejemplo, este script se ejecuta con las credenciales de un usuario llamado kenmyer, con la contraseña homerj.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



También puede usar el formato de \\ nombre de usuario de dominio para especificar un nombre de usuario. Por ejemplo:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de PowerShell se usa **SWbemLocator** para conectarse a un servidor.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




