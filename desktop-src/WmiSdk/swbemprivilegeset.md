---
description: Un objeto SWbemPrivilegeSet es una colección de objetos SWbemPrivilege de un objeto SWbemSecurity que solicita privilegios específicos para un objeto Instrumental de administración de Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objeto SWbemPrivilegeSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360543"
---
# <a name="swbemprivilegeset-object"></a>Objeto SWbemPrivilegeSet

Un objeto **SWbemPrivilegeSet** es una colección de objetos [**SWbemPrivilege**](swbemprivilege.md) de un objeto [**SWbemSecurity**](swbemsecurity.md) que solicita privilegios específicos para un objeto instrumental de administración de Windows (WMI). Consulte la lista de privilegios en las [**constantes de privilegios**](privilege-constants.md). Los elementos se agregan a la colección mediante los métodos [**Add**](swbemprivilegeset-add.md) y [**AddAsString**](swbemprivilegeset-addasstring.md) . Los elementos se recuperan de la colección mediante el método [**Item**](swbemprivilegeset-item.md) y se quitan mediante el método [**Remove**](swbemprivilegeset-remove.md) . Este objeto no se puede crear mediante la llamada al método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript. Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

Un objeto **SWbemPrivilegeSet** es un conjunto de solicitudes de invalidación de privilegios para un objeto específico. Cuando se realiza una llamada API mediante este objeto, se intentan las solicitudes de invalidación de privilegios. El objeto **SWbemPrivilegeSet** no define los privilegios disponibles para el usuario o el proceso actual. En otras palabras, la obtención de los privilegios de cualquier objeto WMI no identifica la configuración de privilegios que se realiza en la conexión a WMI o los privilegios en vigor cuando se entrega un objeto a un receptor.

## <a name="members"></a>Miembros

El objeto **SWbemPrivilegeSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemPrivilegeSet** tiene estos métodos.



| Método                                               | Descripción                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agréguela**](swbemprivilegeset-add.md)                 | Agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la colección **SWbemPrivilegeSet** mediante una constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | Agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la colección **SWbemPrivilegeSet** mediante una cadena de privilegios.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Elimina todos los privilegios de la colección.<br/>                                                                                                              |
| [**Elemento**](swbemprivilegeset-item.md)               | Recupera un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección. Este es el método predeterminado de este objeto.<br/>                                 |
| [**Retirar**](swbemprivilegeset-remove.md)           | Quita un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección.<br/>                                                                              |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemPrivilegeSet** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contabiliza**](swbemprivilegeset-count.md)<br/> | Solo lectura<br/> | Número de elementos de la colección.<br/> |



 

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se obtiene un objeto SWbemPrivileges y se agregan todos los privilegios disponibles a la colección por valor de privilegio, tal y como se define en [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



En el ejemplo de código de VBScript siguiente se muestra cómo agregar privilegios mediante el objeto **SWbemPrivilegeSet** .


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



En el ejemplo de código Perl siguiente se muestra cómo agregar privilegios mediante el objeto **SWbemPrivilegeSet** .


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | \_ISWBEMPRIVILEGESET IID<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejecutar operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> <dt>

[**Constantes de privilegio**](privilege-constants.md)
</dt> </dl>

 

