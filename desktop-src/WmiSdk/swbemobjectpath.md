---
description: Use los métodos y propiedades del objeto SWbemObjectPath para construir y validar una ruta de acceso de objeto. Este objeto se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objeto SWbemObjectPath (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2d7273b39c5cdccea7e46a077c925247846cd9ca255fc1dba20a95aeb159b773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313554"
---
# <a name="swbemobjectpath-object"></a>Objeto SWbemObjectPath

Use los métodos y propiedades del **objeto SWbemObjectPath** para construir y validar una ruta de acceso de objeto. Este objeto se puede crear mediante la llamada **CreateObject de** VBScript.

## <a name="members"></a>Miembros

El **objeto SWbemObjectPath** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemObjectPath** tiene estos métodos.



| Método                                                   | Descripción                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Fuerza a la ruta de acceso a una clase WMI.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Fuerza a la ruta de acceso a una instancia wmi singleton.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemObjectPath** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autoridad**](swbemobjectpath-authority.md)<br/>             | Lectura/escritura<br/> | Cadena que define el componente Authority de la ruta de acceso del objeto.<br/>                                                                                                           |
| [**Clase**](swbemobjectpath-class.md)<br/>                     | Lectura/escritura<br/> | Nombre de la clase que forma parte de la ruta de acceso del objeto.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Lectura/escritura<br/> | Cadena que contiene la ruta de acceso en un formulario que se puede usar como nombre para mostrar de moniker. Consulte [Creación de una aplicación WMI o script.](creating-a-wmi-application-or-script.md)<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Solo lectura<br/>  | Valor booleano que indica si esta ruta de acceso representa una clase. Esto es análogo a la propiedad [ \_ \_ Deserción](wmi-system-properties.md) en la API COM.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Solo lectura<br/>  | Valor booleano que indica si esta ruta de acceso representa una instancia singleton.<br/>                                                                                                |
| [**Claves**](swbemobjectpath-keys.md)<br/>                       | Solo lectura<br/>  | Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contiene los enlaces de valor de clave.<br/>                                                                          |
| [**Configuración regional**](swbemobjectpath-locale.md)<br/>                   | Lectura/escritura<br/> | Cadena que contiene la configuración regional de esta ruta de acceso de objeto.<br/>                                                                                                                     |
| [**Espacio de nombres**](swbemobjectpath-namespace.md)<br/>             | Lectura/escritura<br/> | Nombre del espacio de nombres que forma parte de la ruta de acceso del objeto. Esto es lo mismo que la propiedad [ \_ \_ Namespace](wmi-system-properties.md) de la API COM.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Solo lectura<br/>  | Nombre del elemento primario del espacio de nombres que forma parte de la ruta de acceso del objeto.<br/>                                                                                                      |
| [**Ruta de acceso**](swbemobjectpath-path.md)<br/>                       | Lectura/escritura<br/> | Contiene la ruta de acceso absoluta. Esto es lo mismo que la propiedad [ \_ \_ path del](wmi-system-properties.md) sistema en la API COM. Esta es la propiedad predeterminada de este objeto .<br/>    |
| [**Relpath**](swbemobjectpath-relpath.md)<br/>                 | Lectura/escritura<br/> | Contiene la ruta de acceso relativa. Esto es lo mismo que la propiedad del sistema [ \_ \_ Relpath](wmi-system-properties.md) en la API COM.<br/>                                              |
| [**Seguridad\_**](swbemobjectpath-security-.md)<br/>            | Solo lectura<br/>  | Se usa para leer o cambiar la configuración de seguridad.<br/>                                                                                                                             |
| [**Servidor**](swbemobjectpath-server.md)<br/>                   | Lectura/escritura<br/> | Nombre del servidor. Esto es lo mismo que la propiedad [ \_ \_ Del](wmi-system-properties.md) sistema del servidor en la API COM.<br/>                                                       |



 

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se muestra cómo crear rutas de acceso de objeto.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



En el siguiente ejemplo de código Perl se muestra cómo crear rutas de acceso a objetos.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




