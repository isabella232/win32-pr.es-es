---
description: Los métodos y propiedades del objeto SWbemLastError contienen y manipulan objetos de error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objeto SWbemLastError (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a73312c38857b57f3ffeec8fcaf8a9ea5847001393d0a03d4916da76ffcb8c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314464"
---
# <a name="swbemlasterror-object"></a>Objeto SWbemLastError

Los métodos y propiedades del **objeto SWbemLastError** contienen y manipulan objetos de error. Los métodos y propiedades de este objeto son exactamente iguales que los del objeto [**SWbemObject,**](swbemobject.md) pero se usan para contener información de error en lugar de información de clase WMI. Este objeto se puede crear mediante la llamada **CreateObject de** VBScript.

Puede crear un objeto de error **SWbemLastError** para inspeccionar la información de error extendida asociada a una llamada al método anterior. Si la información de error no está disponible, se producirá un error al intentar crear un objeto de error. Si la llamada se realiza correctamente y se devuelve un objeto de error, se restablece el estado del objeto. Se producirá un error en otros intentos de recuperar un objeto de error hasta que se produzca un nuevo error. Si realiza una llamada asincrónica que produce un error, el evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) puede devolverle un objeto **SWbemLastError** en el parámetro *objWbemErrorObject.*

## <a name="members"></a>Miembros

El **objeto SWbemLastError** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemLastError** tiene estos métodos.



| Método                                                   | Descripción                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **Asociadores\_**                                        | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **AssociatorsAsync\_**                                   | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| [**Clon\_**](swbemlasterror-clone-.md)                 | Realiza una copia del objeto actual.<br/>                                               |
| [**Compareto\_**](swbemlasterror-compareto-.md)         | Comprueba la igualdad de dos objetos.<br/>                                                   |
| **Eliminar\_**                                             | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **DeleteAsync\_**                                        | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **ExecMethod\_**                                         | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **ExecMethodAsync\_**                                    | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Recupera la representación textual del objeto escrito con sintaxis MOF.<br/>       |
| **Instancias\_**                                          | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **InstancesAsync\_**                                     | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **Poner\_**                                                | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **PutAsync\_**                                           | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **Referencias\_**                                         | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **ReferencesAsync\_**                                    | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **SpawnDerivedClass\_**                                  | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **SpawnInstance\_**                                      | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **Subclases \_**                                         | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |
| **SubclassesAsync\_**                                    | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemLastError** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Derivación\_**<br/>                                   | Solo lectura<br/> | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/>                                                                  |
| **Métodos\_** <br/>                                     | Solo lectura<br/> | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/>                                                                  |
| [**Ruta de acceso\_**](swbemlasterror-path-.md)<br/>             | Solo lectura<br/> | Contiene un [**objeto SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual.<br/>                    |
| [**Propiedades\_**](swbemlasterror-properties-.md)<br/> | Solo lectura<br/> | Representa la colección de propiedades del **objeto SWbemLastError.** Esta propiedad es un [**objeto SWbemPropertySet.**](swbempropertyset.md)<br/> |
| **Calificadores\_**<br/>                                   | Solo lectura<br/> | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/>                                                                  |
| **Seguridad\_**<br/>                                     | Solo lectura<br/> | No se usa. El [**objeto SWbemObject**](swbemobject.md) proporciona el mismo método.<br/>                                                                  |



 

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript siguiente se muestra cómo inspeccionar la información del objeto de error y de error.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



En el ejemplo de Perl siguiente se muestra cómo inspeccionar la información del objeto de error y de error.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
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
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




