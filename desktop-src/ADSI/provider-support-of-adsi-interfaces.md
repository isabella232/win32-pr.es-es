---
title: Compatibilidad del proveedor con interfaces ADSI
description: En la tabla siguiente se muestra una breve descripción de las interfaces admitidas por los proveedores incluidos con ADSI para Windows 2000 y DS Client.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Compatibilidad del proveedor con ADSI interfaces ADSI
- ADSI ADSI, proveedores de servicios e interfaces compatibles con cada proveedor
- Compatibilidad del proveedor con IADsUser
- Compatibilidad del proveedor con IADsComputer
- Compatibilidad del proveedor con IADsComputerOperations
- Compatibilidad del proveedor con IADsDomain
- Compatibilidad del proveedor con IADsFileService
- Compatibilidad del proveedor con IADsGroup
- Compatibilidad del proveedor con IADsClass
- Compatibilidad del proveedor con IADsProperty
- Compatibilidad del proveedor con IADsSyntax
- Compatibilidad del proveedor con IADsContainer
- Compatibilidad del proveedor con IADsNamespaces
- Compatibilidad del proveedor con IADsAccessControlEntry
- Compatibilidad del proveedor con IADsAccessControlList
- Compatibilidad del proveedor con IADsSecurityDescriptor
- Compatibilidad del proveedor con IADsObjectOptions
- Compatibilidad del proveedor con IADsCollection
- Compatibilidad del proveedor con IADsMembers
- Compatibilidad del proveedor con IADsPathname
- Compatibilidad del proveedor con IADsPrintQueue
- Compatibilidad del proveedor con IADsPrintQueueOperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174586"
---
# <a name="provider-support-of-adsi-interfaces"></a>Compatibilidad del proveedor con interfaces ADSI

En la tabla siguiente se muestra una breve descripción de las interfaces admitidas por los proveedores incluidos con ADSI para Windows 2000 y DS Client. Una entrada marcada con "Sí" indica que al menos un objeto ADSI del proveedor especificado admite la interfaz asociada. "No" indica que ningún objeto del proveedor admite la interfaz en esta versión. En el futuro, las interfaces actualmente no admitidas pueden ser compatibles con los proveedores proporcionados por el sistema.

Para obtener más información sobre los detalles de implementación específicos del proveedor adsi, consulte:

-   [Proveedor LDAP ADSI](adsi-ldap-provider.md)
-   [Proveedor ADSI WinNT](adsi-winnt-provider.md)
-   [ENRUTADOR ADSI](adsi-router.md)

Para obtener más información sobre qué propiedad o método se admite para cada interfaz, haga clic en el nombre de interfaz adecuado en la primera columna de la tabla.



| Nombre de la interfaz                                                 | LDAP | Winnt |
|----------------------------------------------------------------|------|-------|
| [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Sí  | Sí   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Sí  | No    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Sí  | No    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | No   | No    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | No   | No    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | No   | No    |
| [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Sí  | Sí   |
| [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | No   | Sí   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | No   | Sí   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | No   | Sí   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Sí  | Sí   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Sí  | No    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | No   | Sí   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | No   | No    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Sí  | Sí   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | No   | No    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | No   | Sí   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | No   | Sí   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | No   | Sí   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Sí  | Sí   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | No   | No    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Sí  | No    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Sí  | No    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Sí  | Sí   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Sí  | Sí   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | No   | No    |
| [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Sí  | No    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Sí  | No    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | No   | No    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Sí  | Sí   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Sí  | No    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | No   | No    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Sí  | Sí   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | No   | No    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | No   | Sí   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | No   | Sí   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Sí  | Sí   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Sí  | Sí   |
| [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Sí  | Sí   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Sí  | Sí   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Sí  | Sí   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Sí  | Sí   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Sí  | Sí   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | No   | No    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | No   | Sí   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Sí  | No    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | No   | Sí   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | No   | Sí   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | No   | Sí   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Sí  | Sí   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | No   | No    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | No   | No    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Sí  | Sí   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Sí  | No    |
| [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Sí  | No    |



 

## <a name="provider-support-for-iadsuser"></a>Compatibilidad del proveedor con IADsUser



| Propiedad                                                    | LDAP          | Winnt         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | Compatible     | Compatible     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Compatible     | Compatible     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | No compatible   | No compatible |
| [**BadLoginCount**](iadsuser-property-methods.md)          | Compatible     | Compatible     |
| [**Departamento**](iadsuser-property-methods.md)             | Compatible     | No compatible   |
| [**Descripción**](iadsuser-property-methods.md)            | Compatible     | Compatible     |
| [**División**](iadsuser-property-methods.md)               | Compatible     | No compatible   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Compatible     | No compatible   |
| [**Employeeid**](iadsuser-property-methods.md)             | Compatible     | No compatible   |
| [**FaxNumber**](iadsuser-property-methods.md)              | Compatible     | No compatible   |
| [**FirstName**](iadsuser-property-methods.md)              | Compatible     | No compatible   |
| [**FullName**](iadsuser-property-methods.md)               | Compatible     | Compatible     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | No compatible | No compatible   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | No compatible | No compatible   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Compatible     | Compatible     |
| [**Página principal**](iadsuser-property-methods.md)               | Compatible     | No compatible   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | Compatible     | Compatible     |
| [**Lenguajes**](iadsuser-property-methods.md)              | No compatible | No compatible   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | Compatible     | No compatible   |
| [**LastLogin**](iadsuser-property-methods.md)              | Compatible     | Compatible     |
| [**LastLogoff**](iadsuser-property-methods.md)             | Compatible     | Compatible     |
| [**LastName**](iadsuser-property-methods.md)               | Compatible     | No compatible   |
| [**LoginHours**](iadsuser-property-methods.md)             | Compatible     | Compatible     |
| [**LoginScript**](iadsuser-property-methods.md)            | Compatible     | Compatible     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | Compatible     | Compatible     |
| [**Director**](iadsuser-property-methods.md)                | Compatible     | No compatible   |
| [**MaxLogins**](iadsuser-property-methods.md)              | No compatible   | No compatible   |
| [**MaxStorage**](iadsuser-property-methods.md)             | Compatible     | Compatible     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Compatible     | No compatible   |
| [**Sufijonombre**](iadsuser-property-methods.md)             | Compatible     | No compatible   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | Compatible     | No compatible   |
| [**OtherName**](iadsuser-property-methods.md)              | Compatible     | No compatible   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | No compatible   | Compatible     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | Compatible     | No compatible   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | No compatible   | Compatible     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Compatible     | Compatible     |
| [**Imagen**](iadsuser-property-methods.md)                | Compatible     | No compatible   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | Compatible     | No compatible   |
| [**PostalCodes**](iadsuser-property-methods.md)            | Compatible     | No compatible   |
| [**Perfil**](iadsuser-property-methods.md)                | Compatible     | Compatible     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | No compatible   | No compatible   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Compatible     | No compatible   |
| [**TelephoneHome**](iadsuser-property-methods.md)          | Compatible     | No compatible   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | Compatible     | No compatible   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Compatible     | No compatible   |
| [**TelephonePager**](iadsuser-property-methods.md)         | Compatible     | No compatible   |
| [**Título**](iadsuser-property-methods.md)                  | Compatible     | No compatible   |



 

## <a name="provider-support-for-iadscomputer"></a>Compatibilidad del proveedor con IADsComputer



| Propiedades                                     | LDAP                    | Winnt       |
|------------------------------------------------|-------------------------|-------------|
| [**ComputerID**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaz no admitida | No compatible |
| [**department**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaz no admitida | No compatible |
| [**Descripción**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interfaz no admitida | No compatible |
| [**División**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interfaz no admitida | Compatible   |
| [**Ubicación**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interfaz no admitida | No compatible |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaz no admitida | No compatible |
| [**Modelo**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interfaz no admitida | No compatible |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Interfaz no admitida | No compatible |
| [**OperatingSystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interfaz no admitida | Compatible   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Interfaz no admitida | Compatible   |
| [**Propietario**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interfaz no admitida | Compatible   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interfaz no admitida | No compatible |
| [**Procesador**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Interfaz no admitida | Compatible   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Interfaz no admitida | Compatible   |
| [**Role**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interfaz no admitida | No compatible |
| [**Sitio**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interfaz no admitida | No compatible |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | No se admite la interfaz | No compatible |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Compatibilidad del proveedor con IADsComputerOperations



| Propiedad                                   | LDAP                    | Winnt           |
|--------------------------------------------|-------------------------|-----------------|
| [**Apagado**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | No se admite la interfaz | No implementado |
| [**Estado**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | No se admite la interfaz | No implementado |



 

## <a name="provider-support-for-iadsdomain"></a>Compatibilidad del proveedor con IADsDomain



| Propiedad                                         | LDAP                    | Winnt           |
|--------------------------------------------------|-------------------------|-----------------|
| [**IsWorkgroup**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | No se admite la interfaz | No implementado |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | No se admite la interfaz | Compatible       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | No se admite la interfaz | Compatible       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | No se admite la interfaz | Compatible       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | No se admite la interfaz | Compatible       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | No se admite la interfaz | Compatible       |
| [**PasswordAttributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | No se admite la interfaz | No compatible     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | No se admite la interfaz | Compatible       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | No se admite la interfaz | Compatible       |



 

## <a name="provider-support-for-iadsfileservice"></a>Compatibilidad del proveedor con IADsFileService



| Propiedad                                | LDAP                    | Winnt     |
|-----------------------------------------|-------------------------|-----------|
| [**Descripción**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | No se admite la interfaz | Compatible |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | No se admite la interfaz | Compatible |



 

## <a name="provider-support-for-iadsgroup"></a>Compatibilidad del proveedor con IADsGroup



| Propiedad                         | LDAP      | Winnt     |
|----------------------------------|-----------|-----------|
| [**Descripción**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Compatible | Compatible |



 

## <a name="provider-support-for-iadsclass"></a>Compatibilidad del proveedor con IADsClass



| Propiedad                                   | LDAP               | Winnt           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Compatible          | Compatible       |
| [**CLSID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Compatible          | Compatible       |
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Compatible          | Compatible       |
| [**Descripción breve**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Compatible          | Compatible       |
| [**Auxiliar**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Compatible          | Compatible       |
| [**Propiedades obligatorias**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Compatible          | Compatible       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Compatible          | Compatible       |
| [**NamingProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Compatible          | No implementado |
| [**DerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Compatible          | No compatible     |
| [**AuxiliarDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Compatible          | No compatible     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Compatible          | Compatible       |
| [**Containment**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Compatible con lectura | Compatible       |
| [**Contenedor**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Compatible con lectura | Compatible       |
| [**HelpFileName**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Compatible          | Compatible       |
| [**HelpFileContext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Compatible          | Compatible       |
| Método                                     | LDAP               | Winnt           |
| [**Calificadores**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | No implementado    | No implementado |



 

## <a name="provider-support-for-iadsproperty"></a>Compatibilidad del proveedor con IADsProperty



| Propiedad                            | LDAP      | Winnt     |
|-------------------------------------|-----------|-----------|
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Compatible | Compatible |
| [**Sintaxis**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Compatible | Compatible |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Compatible | Compatible |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Compatible | Compatible |
| [**Multivalor**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Compatible | Compatible |



 

## <a name="provider-support-for-iadssyntax"></a>Compatibilidad del proveedor con IADsSyntax



| Propiedad                              | LDAP      | Winnt     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Compatible | Compatible |



 

## <a name="provider-support-for-iadscontainer"></a>Compatibilidad del proveedor con IADsContainer



| Propiedad                        | LDAP            | Winnt           |
|---------------------------------|-----------------|-----------------|
| [**Count**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | No implementado | No implementado |
| [**Sugerencias**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Compatible       | No implementado |
| [**Filtro**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Compatible       | Compatible       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Compatibilidad del proveedor con IADsNamespaces



| Propiedad                                   | LDAP      | Winnt     |
|--------------------------------------------|-----------|-----------|
| [**defaultContainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Compatible | Compatible |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Compatibilidad del proveedor con IADsAccessControlEntry



| Propiedad                                              | LDAP      | Winnt       |
|-------------------------------------------------------|-----------|-------------|
| [**Máscara de acceso**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Compatible | No compatible |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Compatible | No compatible |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Compatible | No compatible |
| [**Marcas**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Compatible | No compatible |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Compatible | No compatible |
| [**InheritedObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Compatible | No compatible |
| [**Fideicomisario**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Compatible | No compatible |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Compatibilidad del proveedor con IADsAccessControlList



| Propiedad                                                       | LDAP      | Winnt       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Compatible | No compatible |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Compatible | No compatible |
| Método                                                         | LDAP      | Winnt       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Compatible | No compatible |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Compatible | No compatible |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Compatible | No compatible |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Compatible | No compatible |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Compatibilidad del proveedor con IADsSecurityDescriptor



| Propiedad                                                                        | LDAP      | Winnt       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Control**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Compatible | No compatible |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Compatible | No compatible |
| [**DiscretionaryAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Compatible | No compatible |
| [**Group (Grupo)**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Compatible | No compatible |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Compatible | No compatible |
| [**Propietario**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Compatible | No compatible |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Compatible | No compatible |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Compatible | No compatible |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Compatible | No compatible |
| Método                                                                          | LDAP      | Winnt       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Compatible | No compatible |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Compatibilidad del proveedor con IADsObjectOptions



| Método                                           | LDAP      | Winnt                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Compatible | Interfaz no admitida |
| [**Setoption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Compatible | Interfaz no admitida |



 

## <a name="provider-support-for-iadscollection"></a>Compatibilidad del proveedor con IADsCollection



| Método                                                | LDAP                    | Winnt       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Add (Agregar)**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Interfaz no admitida | No compatible |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Interfaz no admitida | Compatible   |
| [**Getobject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Interfaz no admitida | Compatible   |
| [**Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Interfaz no admitida | Compatible   |



 

## <a name="provider-support-for-iadsmembers"></a>Compatibilidad del proveedor con IADsMembers



| Propiedad                                           | LDAP                                                      | Winnt       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Count**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Compatible con GroupCollection, pero no con UserCollection | No compatible |
| [**Filtro**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Compatible                                                 | Compatible   |
| Método                                             | LDAP                                                      | Winnt       |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Compatible                                                 | Compatible   |



 

## <a name="provider-support-for-iadspathname"></a>Compatibilidad del proveedor con IADsPathname



| Propiedad                                                    | LDAP      | Winnt       |
|-------------------------------------------------------------|-----------|-------------|
| [**EscapedMode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Compatible | Compatible   |
| Método                                                      | LDAP      | Winnt       |
| [**Establecer**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Compatible | Compatible   |
| [**SetDisplayType**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Compatible | Compatible   |
| [**Recuperar**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Compatible | Compatible   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Compatible | Compatible   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Compatible | Compatible   |
| [**GetEscapedElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Compatible | No compatible |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Compatible | Compatible   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Compatible | Compatible   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Compatibilidad del proveedor con IADsPrintQueue



| Propiedad                                     | LDAP        | Winnt       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Compatible   | No compatible |
| [**Modelo**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Compatible   | Compatible.  |
| [**Datatype**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | No compatible | Compatible   |
| [**PrintProcessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | No compatible | Compatible   |
| [**Descripción**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Compatible   | Compatible   |
| [**Ubicación**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Compatible   | Compatible   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Compatible   | Compatible   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Compatible   | Compatible   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | No compatible | Compatible   |
| [**Priority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Compatible   | Compatible   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Compatible   | Compatible   |
| [**PrintDevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Compatible   | Compatible   |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | No compatible | No compatible |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Compatibilidad del proveedor con IADsPrintQueueOperations



| Propiedad                                                | LDAP      | Winnt      |
|---------------------------------------------------------|-----------|------------|
| [**Estado**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Compatible | Compatible  |
| Método                                                  | LDAP      | Winnt      |
| [**Pausar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Compatible | Compatible. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Compatible | Compatible  |
| [**Purgar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Compatible | Compatible  |
| [**Reanudar**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Compatible | Compatible  |



 

 

 




