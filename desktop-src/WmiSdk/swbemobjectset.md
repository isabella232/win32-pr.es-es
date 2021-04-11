---
description: Un objeto SWbemObjectSet es una colección de objetos SWbemObject. Para obtener más información, vea obtener acceso a una colección. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objeto SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279100"
---
# <a name="swbemobjectset-object"></a>Objeto SWbemObjectSet

Un objeto **SWbemObjectSet** es una colección de objetos [**SWbemObject**](swbemobject.md) . Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md). Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.

Puede obtener un objeto **SWbemObjectSet** llamando a cualquiera de los métodos siguientes o a sus equivalentes asincrónicos:

-   [**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
-   [**SWbemObject. instances\_**](swbemobject-instances-.md)
-   [**SWbemObject. References\_**](swbemobject-references-.md)
-   [**SWbemObject. subclases\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. instances**](swbemservices-instancesof.md)
-   [**SWbemServices. References**](swbemservices-referencesto.md)
-   [**SWbemServices. subclasses**](swbemservices-subclassesof.md)

> [!Note]  
> El objeto **SWbemObjectSet** no admite los métodos opcionales para **Agregar** y **quitar** colecciones.

 

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

## <a name="members"></a>Miembros

El objeto **SWbemObjectSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemObjectSet** tiene estos métodos.



| Método                              | Descripción                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Elemento**](swbemobjectset-item.md) | Recupera un objeto [**SWbemObject**](swbemobject.md) de la colección. Este es el método predeterminado del objeto.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemObjectSet** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso          | Descripción                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Contabiliza**](swbemobjectset-count.md)<br/>          | Solo lectura<br/> | Número de elementos de la colección.<br/>        |
| [**Seguridad\_**](swbemobjectset-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="remarks"></a>Observaciones

Un **SWbemObjectSet** es una colección de cero o más objetos [**SWbemObject**](swbemobject.md) . Cada **SWbemObject** de un **SWbemObjectSet** puede representar una de estas dos cosas:

-   Instancia de un recurso administrado por WMI.
-   Una instancia de una definición de clase.

El uso más común de esta clase en WMI es como el valor devuelto para una llamada a [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) o a [**instancias**](swbemservices-instancesof.md) , como se describe en el ejemplo de código siguiente:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



En su mayor parte, lo único que tendrá que hacer con un **SWbemObjectSet** es enumerar todos los objetos contenidos en la propia colección. Sin embargo, **SWbemObjectSet** incluye un recuento de propiedades que puede ser útil en el scripting de administración del sistema. Como implica el nombre, Count indica el número de elementos de la colección. Por ejemplo, este script recupera una colección de todos los servicios instalados en un equipo y, a continuación, devuelve el número total de servicios encontrados:

Para obtener más información sobre cómo usar esta clase, consulte [enumeración de WMI](enumerating-wmi.md).

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código VBScript muestra cómo se manipulan las colecciones **SWbemObjectSet** .


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



El siguiente ejemplo de código Perl muestra cómo se manipulan las colecciones **SWbemObjectSet** .


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




