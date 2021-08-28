---
description: Un objeto SWbemObjectSet es una colección de objetos SWbemObject. Para obtener más información, vea Acceso a una colección. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objeto SWbemObjectSet (Wbemdisp.h)
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
ms.openlocfilehash: 33cefd39dc0e860906bc99b1f591a87dae845d6a9317410ce4850fb1a54ea708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857105"
---
# <a name="swbemobjectset-object"></a>Objeto SWbemObjectSet

Un **objeto SWbemObjectSet** es una colección de [**objetos SWbemObject.**](swbemobject.md) Para obtener más información, vea [Acceso a una colección](accessing-a-collection.md). La llamada **CreateObject** de VBScript no puede crear este objeto.

Puede obtener un objeto **SWbemObjectSet** llamando a cualquiera de los métodos siguientes o sus equivalentes asincrónicos:

-   [**SWbemObject.Associators\_**](swbemobject-associators-.md)
-   [**SWbemObject.Instances\_**](swbemobject-instances-.md)
-   [**SWbemObject.References\_**](swbemobject-references-.md)
-   [**SWbemObject.Subclasses\_**](swbemobject-subclasses-.md)
-   [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> El **objeto SWbemObjectSet** no admite los métodos de colección **Add** y **Remove** opcionales.

 

> [!Note]  
> Dado que es posible que la llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

## <a name="members"></a>Miembros

El **objeto SWbemObjectSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemObjectSet** tiene estos métodos.



| Método                              | Descripción                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Elemento**](swbemobjectset-item.md) | Recupera un [**objeto SWbemObject**](swbemobject.md) de la colección. Este es el método predeterminado del objeto .<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemObjectSet** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso          | Descripción                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Count**](swbemobjectset-count.md)<br/>          | Solo lectura<br/> | Número de elementos de la colección.<br/>        |
| [**Seguridad\_**](swbemobjectset-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="remarks"></a>Comentarios

Un **SWbemObjectSet** es una colección de cero o más [**objetos SWbemObject.**](swbemobject.md) Cada **SWbemObject** de **SWbemObjectSet** puede representar una de estas dos cosas:

-   Instancia de un recurso administrado por WMI.
-   Instancia de una definición de clase.

El uso más común de esta clase en WMI es como valor devuelto para una llamada [**a ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) o [**InstancesOf,**](swbemservices-instancesof.md) como se describe en el ejemplo de código siguiente:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



En su mayor parte, lo único que hará con **un SWbemObjectSet** es enumerar todos los objetos incluidos en la propia colección. Sin embargo, **SWbemObjectSet incluye** una propiedad Count que puede ser útil en el scripting de administración del sistema. Como su nombre implica, Count indica el número de elementos de la colección. Por ejemplo, este script recupera una colección de todos los servicios instalados en un equipo y, a continuación, hace eco del número total de servicios encontrados:

Para obtener más información sobre cómo usar esta clase, vea [Enumerar WMI.](enumerating-wmi.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo se manipulan las colecciones **SWbemObjectSet.**


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



En el ejemplo de código perl siguiente se muestra cómo se manipulan las colecciones **SWbemObjectSet.**


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




