---
title: posixGroup (clase)
description: Representa una abstracción de un grupo de cuentas.
ms.assetid: d6fa3aab-cb98-4774-b419-afae975c6917
ms.tgt_platform: multiple
keywords:
- posixGroup class AD Schema
topic_type:
- apiref
api_name:
- posixGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3787ae7f918c9829de61a15ed146adc6bc19a178019304cc3f38894e9afd5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680510"
---
# <a name="posixgroup-class"></a>posixGroup (clase)

Representa una abstracción de un grupo de cuentas.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | posixGroup                           |
| Ldap-Display-Name | posixGroup                           |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | 2a9350b8-062c-4ed0-9903-dde10d06deba |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 3                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Superior**](c-top.md)<br/>                                                              |
| Posibles superiores          | \-                                                                                           |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                                   |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre común**](a-cn.md)                                                 | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Descripción**](a-description.md)                                        | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas**](a-flags.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                            | Falso     | **posixGroup**                                 |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Superior**](c-top.md)<br/>                |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**memberUid**](a-memberuid.md)                                            | Falso     | **posixGroup**                                 |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Superior**](c-top.md)<br/>                |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Superior**](c-top.md)<br/>                |
| [**Object-Class**](a-objectclass.md)                                       | True      | [**Superior**](c-top.md)<br/>                |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**unixUserPassword**](a-unixuserpassword.md)                              | Falso     | **posixGroup**                                 |
| [**Contraseña de usuario**](a-userpassword.md)                                     | Falso     | **posixGroup**                                 |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Creado por USN**](a-usncreated.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 3                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Superior**](c-top.md)<br/>                                                              |
| Posibles superiores          | \-                                                                                           |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                   |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                    | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Descripción**](a-description.md)                                           | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre de extensión**](a-extensionname.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas**](a-flags.md)                                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Desde entrada**](a-fromentry.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                               | Falso     | **posixGroup**                                 |
| [**Tipo de instancia**](a-instancetype.md)                                        | True      | [**Superior**](c-top.md)<br/>                |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se elimina**](a-isdeleted.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos administrados**](a-managedobjects.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**memberUid**](a-memberuid.md)                                               | Falso     | **posixGroup**                                 |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | True      | [**Superior**](c-top.md)<br/>                |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Category**](a-objectcategory.md)                                    | True      | [**Superior**](c-top.md)<br/>                |
| [**Object-Class**](a-objectclass.md)                                          | True      | [**Superior**](c-top.md)<br/>                |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Version**](a-objectversion.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Informes**](a-directreports.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Revisión**](a-revision.md)                                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Sub refs**](a-subrefs.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas del sistema**](a-systemflags.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**unixUserPassword**](a-unixuserpassword.md)                                 | Falso     | **posixGroup**                                 |
| [**Contraseña de usuario**](a-userpassword.md)                                        | Falso     | **posixGroup**                                 |
| [**USN cambiado**](a-usnchanged.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Creado por USN**](a-usncreated.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuando se crea**](a-whencreated.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 3                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Superior**](c-top.md)<br/>                                                              |
| Posibles superiores          | \-                                                                                           |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                   |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                      | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Descripción**](a-description.md)                                             | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas**](a-flags.md)                                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | **posixGroup**                                 |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Superior**](c-top.md)<br/>                |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | **posixGroup**                                 |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Superior**](c-top.md)<br/>                |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Superior**](c-top.md)<br/>                |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Superior**](c-top.md)<br/>                |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | **posixGroup**                                 |
| [**Contraseña de usuario**](a-userpassword.md)                                          | Falso     | **posixGroup**                                 |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Creado por USN**](a-usncreated.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos conocidos**](a-wellknownobjects.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 3                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Superior**](c-top.md)<br/>                                                              |
| Posibles superiores          | \-                                                                                           |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                   |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                                  | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Descripción**](a-description.md)                                                         | Falso     | **posixGroup** [ **Top**](c-top.md)<br/> |
| [**Nombre para mostrar**](a-displayname.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Nombre de extensión**](a-extensionname.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas**](a-flags.md)                                                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Desde entrada**](a-fromentry.md)                                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                                             | Falso     | **posixGroup**                                 |
| [**Tipo de instancia**](a-instancetype.md)                                                      | True      | [**Superior**](c-top.md)<br/>                |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se elimina**](a-isdeleted.md)                                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Se recicla**](a-isrecycled.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Objetos administrados**](a-managedobjects.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**memberUid**](a-memberuid.md)                                                             | Falso     | **posixGroup**                                 |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | True      | [**Superior**](c-top.md)<br/>                |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Category**](a-objectcategory.md)                                                  | True      | [**Superior**](c-top.md)<br/>                |
| [**Object-Class**](a-objectclass.md)                                                        | True      | [**Superior**](c-top.md)<br/>                |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Object-Version**](a-objectversion.md)                                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Informes**](a-directreports.md)                                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Revisión**](a-revision.md)                                                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                               | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Sub refs**](a-subrefs.md)                                                                | Falso     | [**Superior**](c-top.md)<br/>                |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Marcas del sistema**](a-systemflags.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falso     | **posixGroup**                                 |
| [**Contraseña de usuario**](a-userpassword.md)                                                      | Falso     | **posixGroup**                                 |
| [**USN cambiado**](a-usnchanged.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**UsN creado**](a-usncreated.md)                                                          | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Superior**](c-top.md)<br/>                |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**Cuando se crea**](a-whencreated.md)                                                        | Falso     | [**Superior**](c-top.md)<br/>                |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                       | Falso     | [**Superior**](c-top.md)<br/>                |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Superior**](c-top.md)<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RFC 2307](https://www.ietf.org/rfc/rfc2307.txt)
</dt> </dl>

 

 





