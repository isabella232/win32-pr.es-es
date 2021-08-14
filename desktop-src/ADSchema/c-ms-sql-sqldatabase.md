---
title: Clase MS-SQL-SQLDatabase
description: Clase para almacenar las SQL Server de base de datos.
ms.assetid: ad1d7532-534a-4220-8e19-70f7c6f36e36
ms.tgt_platform: multiple
keywords:
- Esquema de AD de la clase MS-SQL-SQLDatabase
- mS-SQL-SQLDatabase class AD Schema
topic_type:
- apiref
api_name:
- MS-SQL-SQLDatabase
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 171d87cb075c2efcae7495c0a2625b350bfe42590f1312737600865dc268ee3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441195"
---
# <a name="ms-sql-sqldatabase-class"></a>Clase MS-SQL-SQLDatabase

Clase para almacenar las SQL Server de base de datos.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-SQL-SQLDatabase                   |
| Ldap-Display-Name | mS-SQL-SQLDatabase                   |
| Privilegio actualizar  | El sistema establece este valor.     |
| Frecuencia de actualización  | En la configuración del sistema.                     |
| Schema-Id-Guid    | 1d08694a-ccef-11d2-9993-0000f87a57d4 |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows atributos de servidor 2000

Esta clase contiene los siguientes atributos para Windows 2000 Server:



| Atributo                                                                 | Mandatory | Derivado de                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                   | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                    | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                  | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                              | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                  | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)          | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                  | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                               | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                     | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones proxy**](a-proxyaddresses.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Creado por USN**](a-usncreated.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos conocidos**](a-wellknownobjects.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                           | False     | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                  | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                          | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                    | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                    | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)            | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                    | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                                 | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                       | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Creado por USN**](a-usncreated.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre común**](a-cn.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                      | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                  | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                          | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                    | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                    | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)            | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                        | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                    | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                                 | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                       | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**UsN creado**](a-usncreated.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | False     | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                        | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                     | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                       | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                   | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                       | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)               | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                       | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                                    | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                          | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Creado por USN**](a-usncreated.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                | False     | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre común**](a-cn.md)                                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Se recicla**](a-isrecycled.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                       | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                               | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                     | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)                 | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                         | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                                      | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                            | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Creado por USN**](a-usncreated.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos conocidos**](a-wellknownobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.188                                                                       |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)                                               |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los atributos siguientes para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Descripción**](a-description.md)                                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Banderas**](a-flags.md)                                                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Desde entrada**](a-fromentry.md)                                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Tipo de instancia**](a-instancetype.md)                                                      | True      | [**Arriba**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**Se elimina**](a-isdeleted.md)                                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Se recicla**](a-isrecycled.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Objetos administrados**](a-managedobjects.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Arriba**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**MS-SQL-Alias**](a-ms-sql-alias.md)                                                       | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Applications**](a-ms-sql-applications.md)                                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Contact**](a-ms-sql-contact.md)                                                   | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-CreationDate**](a-ms-sql-creationdate.md)                                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Description**](a-ms-sql-description.md)                                           | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-InformationURL**](a-ms-sql-informationurl.md)                                     | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Keywords**](a-ms-sql-keywords.md)                                                 | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastBackupDate**](a-ms-sql-lastbackupdate.md)                                     | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-LastDiagnosticDate**](a-ms-sql-lastdiagnosticdate.md)                             | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Name**](a-ms-sql-name.md)                                                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Size**](a-ms-sql-size.md)                                                         | False     | **MS-SQL-SQLDatabase**          |
| [**MS-SQL-Status**](a-ms-sql-status.md)                                                     | False     | **MS-SQL-SQLDatabase**          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Category**](a-objectcategory.md)                                                  | True      | [**Arriba**](c-top.md)<br/> |
| [**Object-Class**](a-objectclass.md)                                                        | True      | [**Arriba**](c-top.md)<br/> |
| [**Guid de objeto**](a-objectguid.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**Object-Version**](a-objectversion.md)                                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Arriba**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Arriba**](c-top.md)<br/> |
| [**Informes**](a-directreports.md)                                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**Revisión**](a-revision.md)                                                               | False     | [**Arriba**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | False     | [**Arriba**](c-top.md)<br/> |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                               | False     | [**Arriba**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**Sub refs**](a-subrefs.md)                                                                | False     | [**Arriba**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Marcas del sistema**](a-systemflags.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**USN cambiado**](a-usnchanged.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**UsN creado**](a-usncreated.md)                                                          | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                                      | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | False     | [**Arriba**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                            | False     | [**Arriba**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                              | False     | [**Arriba**](c-top.md)<br/> |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**Cuando se crea**](a-whencreated.md)                                                        | False     | [**Arriba**](c-top.md)<br/> |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                       | False     | [**Arriba**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                              | False     | [**Arriba**](c-top.md)<br/> |



 

 





