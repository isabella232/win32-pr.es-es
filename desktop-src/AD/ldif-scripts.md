---
title: Scripts LDIF
description: El formato de intercambio de datos LDAP (LDIF) es un estándar de Internet Engineering Task Force (IETF) que define cómo importar y exportar los datos de directorio entre los servidores de directorio que usan proveedores de servicios LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory de scripts LDIF
- Scripts LDIF Active Directory, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994971"
---
# <a name="ldif-scripts"></a>Scripts LDIF

El formato de intercambio de datos LDAP (LDIF) es un estándar de Internet Engineering Task Force (IETF) que define cómo importar y exportar los datos de directorio entre los servidores de directorio que usan proveedores de servicios LDAP. Windows 2000 y Windows Server 2003 incluyen una utilidad de línea de comandos, LDIFDE, que se puede usar para importar objetos de directorio en Active Directory Domain Services mediante archivos LDIF. LDIFDE permite establecer un filtro en una cadena específica para buscar y enumerar objetos de directorio en Active Directory Domain Services como archivos LDIF que los administradores de esquema pueden leer fácilmente.

Al importar un archivo Unicode, LDIFDE importa el archivo como Unicode si contiene el identificador Unicode al principio del archivo. Si desea importar un archivo como Unicode cuando no contiene el identificador Unicode al principio del archivo, puede usar el modificador-u para obligar a que se importe como Unicode de.

El modo predeterminado para exportar archivos es ANSI. Si hay entradas Unicode, se convertirán al formato 64 de base. Para exportar un archivo al formato Unicode, use el modificador-u.

Un archivo LDIF debe aplicar cambios de esquema cuando hay dependencias entre los atributos que se agregan. Por ejemplo, los atributos de vínculo hacia delante deben agregarse antes del atributo de vínculo de retroceso correspondiente. También debe actualizar la caché de esquema antes de agregar clases que dependan de atributos o clases agregadas anteriormente en el script LDIF. Para obtener más información, vea el siguiente ejemplo de código.

Tenga en cuenta que para los valores binarios, debe codificar los valores como Base64. La codificación Base64 se define en IETF RFC 2045, sección 6,8.

Para obtener más información sobre el formato de los archivos LDIF, vea [el formato de intercambio de datos LDAP (LDIF): Especificación técnica](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) en el sitio web de Internet Engineering Task Force.

## <a name="ntds-specific-ldif-changetypes"></a>Changetypes LDIF específico de NTDS

Es mejor usar ntdsSchema \* changetypes en lugar de llamar a LDIFDE-k. La opción-k de LDIFDE omite un conjunto mayor de errores LDAP. La lista completa de errores omitidos es la siguiente:

-   El objeto ya es miembro del grupo.
-   Una infracción de clase de objeto (lo que significa que la clase de objeto especificada no existe) si el objeto que se importa no tiene otros atributos.
-   el objeto ya existe (**LDAP \_ ya \_ existe**)
-   infracción de restricción (**\_ \_ infracción de restricción LDAP**)
-   el atributo o valor ya existe **( \_ existe el atributo \_ o el \_ valor \_ LDAP**)
-   no se trata de un objeto de este tipo (**LDAP \_ no es \_ tal \_**)

Los siguientes changetypes están diseñados específicamente para las operaciones de actualización del esquema.



| ChangeType                      | Descripción                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd** se corresponde con **Agregar** en un archivo LDIF. La única diferencia es que **ntdsSchemaAdd** haría que LDIFDE omitiera una operación de **adición** si el objeto ya existe en el esquema. (**LDAP \_ ya \_ existe** se omite).<br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** se corresponde con la **modificación** en un archivo LDIF. La única diferencia es que **ntdsSchemaModify** haría que LDIFDE omitira una operación de **modificación** si el objeto no se encuentra en el esquema. (**LDAP \_ no se omite \_ este \_ objeto** ).<br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete** corresponde a **Delete** en un archivo LDIF. La única diferencia es que **ntdsSchemaDelete** haría que LDIFDE omitira una operación de **eliminación** si el objeto no se encuentra en el esquema. (**LDAP \_ no se omite \_ este \_ objeto** ).<br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** corresponde a **modrdn** en un archivo LDIF. La única diferencia es que **ntdsSchemaModRdn** haría que LDIFDE omitira una operación de nombre distintivo de modificación relativa si el objeto no se encuentra en el esquema. (**LDAP \_ no se omite \_ este \_ objeto** ).<br/> |



 

## <a name="example"></a>Ejemplo

El siguiente ejemplo de código incluye:

-   Myschemaext. ldf es un script LDIF que contiene nuevos atributos y clases. Tenga en cuenta que este archivo es una versión modificada del archivo generado a partir de Lgetattcls.vbs. Tenga en cuenta también que el atributo **My-test-Attribute-DN-FL** se ha desplazado por delante de **My-test-Attribute-DN-BL** porque el vínculo de retroceso (**My-test-Attribute-DN-BL**) depende del vínculo hacia delante (**My-test-Attribute-DN-FL**). Además, el atributo operativo **schemaUpdateNow** se establece en dos lugares para desencadenar actualizaciones de la caché de esquema de modo que los atributos y las clases dependientes estén disponibles para agregar las dos clases en el script.
    > [!Note]  
    > Vea el tema [obtener un identificador de vínculo](obtaining-a-link-id.md) para obtener información sobre el origen del identificador en las instrucciones LinkId:.

     

-   Lgetattcls.vbs es un archivo de VBScript que genera el script LDIF que se usa como punto de partida para Myschemaext. ldf. Tenga en cuenta que la ruta de acceso del esquema actual se ha reemplazado por CN = Schema, CN = Configuration, DC = myorg, DC = com. Puede reemplazar DC = myorg, DC = com para reflejar el nombre distintivo (DN) que se va a publicar en el script LDIF. Asegúrese de que LSETATTCLS.VBS refleje el cambio en su **sFromDN** para que el DN correcto se reemplace cuando se aplique el script LDIF. Tenga en cuenta también que el script usa un prefijo para buscar las clases y los atributos que también debe definir y usar un prefijo para todas las clases y atributos. Para obtener más información, vea [naming Attributes and classes](naming-attributes-and-classes.md). Además, el script genera solo los atributos necesarios para los objetos **attributeSchema** y **ClassSchema** en el archivo LDIF.
-   Lsetattcls.vbs es un archivo de VBScript que usa el script Myschemaext. ldf para agregar los nuevos atributos y clases en el script. Asegúrese de que se puede escribir en el maestro de esquema antes de ejecutar el script.

## <a name="myschemaextldf"></a>MYSCHEMAEXT. LDF

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





