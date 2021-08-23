---
description: Puede usar los métodos del objeto SWbemLocator para obtener un objeto SWbemServices que represente una conexión a un espacio de nombres en un equipo local o en un equipo host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objeto SWbemLocator (Wbemdisp.h)
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
ms.openlocfilehash: 0e93e9bd0bfb33c495b30afbde47bcb9b007acb4cd00dece42e1a8c3b88e99d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732796"
---
# <a name="swbemlocator-object"></a>Objeto SWbemLocator

Puede usar los métodos del objeto **SWbemLocator** para obtener un objeto [**SWbemServices**](swbemservices.md) que represente una conexión a un espacio de nombres en un equipo local o en un equipo host remoto. A continuación, puede usar los métodos del **objeto SWbemServices** para tener acceso a WMI. Este objeto se puede crear mediante la llamada **CreateObject de** VBScript.

## <a name="members"></a>Miembros

El **objeto SWbemLocator** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemLocator** tiene estos métodos.



| Método                                              | Descripción                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Se conecta a WMI en el equipo especificado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemLocator** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso          | Descripción                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Seguridad\_**](swbemlocator-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="remarks"></a>Comentarios

En la parte superior del modelo de objetos de biblioteca de scripting WMI se encuentra el objeto SWbemLocator. SWbemLocator se usa para establecer una conexión autenticada a un espacio de nombres WMI, de la forma en que la función GetObject de VBScript y el moniker WMI "winmgmts:" se usan para establecer una conexión autenticada a WMI. Sin embargo, SWbemLocator está diseñado para abordar dos escenarios de scripting específicos que no se pueden realizar mediante GetObject y el moniker WMI. Debe usar SWbemLocator si necesita:

-   Proporcione credenciales de usuario y contraseña para conectarse a WMI en un equipo remoto. El moniker WMI usado con la función GetObject no incluye un mecanismo para especificar las credenciales. La mayoría de las actividades wmi (incluidas todas las realizadas en equipos remotos) requieren derechos de administrador. Si normalmente inicia sesión con una cuenta de usuario normal en lugar de una cuenta de administrador, no podrá realizar la mayoría de las tareas de WMI a menos que ejecute el script con credenciales alternativas.
-   Conectar a WMI si está ejecutando un script WMI desde una página web. No se puede usar la función GetObject al ejecutar scripts insertados en una página HTML porque Internet Explorer no permite el uso de GetObject por motivos de seguridad.

Además, puede usar SWbemLocator para conectarse a WMI si encuentra la cadena de conexión WMI usada con GetObject confusa o difícil.

Use CreateObject en lugar de GetObject para crear una referencia a SWbemLocator. Para crear la referencia, debe pasar a la función CreateObject el identificador de programación SWbemLocator (ProgID) "WbemScripting.SWbemLocator", como se muestra en la línea 2 del siguiente ejemplo de script. Después de obtener una referencia a un objeto SWbemLocator, llame al método ConnectServer para conectarse a WMI y obtener una referencia a un objeto SWbemServices. Esto se muestra en la línea 3 del siguiente script.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Para ejecutar un script con credenciales alternativas, incluya el nombre de usuario y la contraseña como parámetros adicionales pasados a ConnectServer. Por ejemplo, este script se ejecuta con las credenciales de un usuario llamado kenmyer, con la contraseña homerj.


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



También puede usar el formato nombre \\ de usuario de dominio para especificar un nombre de usuario. Por ejemplo:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de PowerShell se **usa SWbemLocator** para conectarse a un servidor.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




