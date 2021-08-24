---
title: Top (clase)
description: Clase de nivel superior de la que se derivan todas las clases.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de primera clase
- Esquema de AD de clase superior
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248726d9fac9c0d39fae5759df08d4ea10f4f012ba1a1ce0cc2f4dbe55d76a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580595"
---
# <a name="top-class"></a>Top (clase)

Clase de nivel superior de la que se derivan todas las clases.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Superior                                  |
| Ldap-Display-Name | top                                  |
| Actualizar privilegios  | Administrador de esquemas                 |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows de servidor 2000

Esta clase contiene los siguientes atributos para Windows 2000 Server:



| Atributo                                                                 | Mandatory | Derivado de |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                           | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | **Top** (Principales)      |
| [**Common-Name**](a-cn.md)                                               | Falso     | **Top** (Principales)      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                      | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                     | Falso     | **Top** (Principales)      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                 | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                  | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                         | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                   | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                         | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                            | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                               | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | **Top** (Principales)      |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                            | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                               | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                     | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                       | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                 | Falso     | **Top** (Principales)      |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)               | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                         | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | **Top** (Principales)      |
| [**Direcciones de proxy**](a-proxyaddresses.md)                               | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                     | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                        | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                               | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                            | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | **Top** (Principales)      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                             | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                     | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                       | Falso     | **Top** (Principales)      |
| [**Creado por USN**](a-usncreated.md)                                       | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | **Top** (Principales)      |
| [**Objetos conocidos**](a-wellknownobjects.md)                          | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                     | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                     | Falso     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | **Top** (Principales)      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los atributos siguientes para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top** (Principales)      |
| [**Common-Name**](a-cn.md)                                                 | Falso     | **Top** (Principales)      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | **Top** (Principales)      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                    | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top** (Principales)      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top** (Principales)      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top** (Principales)      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top** (Principales)      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top** (Principales)      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                          | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top** (Principales)      |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | **Top** (Principales)      |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | **Top** (Principales)      |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top** (Principales)      |



## <a name="adam"></a>Adán

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|------------------------------------------|
| System-Only                 | Verdadero                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Valor predeterminado de ocultación        | 1                                        |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>   |
| Subclase de                 | **Top** (Principales)<br/>                       |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md) |
| Clases auxiliares           | \-                                       |
| NT-Security-Descriptor      | O:BAG:BAD:S:                             |
| Descriptor de seguridad predeterminado | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Atributos ADAM

Esta clase contiene los atributos siguientes para ADAM:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                 | Falso     | **Top** (Principales)      |
| [**Crear marca de tiempo**](a-createtimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top** (Principales)      |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top** (Principales)      |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top** (Principales)      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | **Top** (Principales)      |
| [**Creado por USN**](a-usncreated.md)                                         | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | **Top** (Principales)      |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top** (Principales)      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top** (Principales)      |
| [**Common-Name**](a-cn.md)                                                 | Falso     | **Top** (Principales)      |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                    | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                    | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top** (Principales)      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falso     | **Top** (Principales)      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top** (Principales)      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | **Top** (Principales)      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top** (Principales)      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top** (Principales)      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top** (Principales)      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top** (Principales)      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | **Top** (Principales)      |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                 | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top** (Principales)      |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                          | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top** (Principales)      |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | **Top** (Principales)      |
| [**Creado por USN**](a-usncreated.md)                                         | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top** (Principales)      |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top** (Principales)      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | **Top** (Principales)      |
| [**Common-Name**](a-cn.md)                                                    | Falso     | **Top** (Principales)      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                           | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                          | Falso     | **Top** (Principales)      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                      | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                       | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                              | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                        | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                              | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                    | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | **Top** (Principales)      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | **Top** (Principales)      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | **Top** (Principales)      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | **Top** (Principales)      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | **Top** (Principales)      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | **Top** (Principales)      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | **Top** (Principales)      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | **Top** (Principales)      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | **Top** (Principales)      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | **Top** (Principales)      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | **Top** (Principales)      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | **Top** (Principales)      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                    | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                          | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                      | Falso     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                          | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                             | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                 | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | **Top** (Principales)      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                                  | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                          | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                            | Falso     | **Top** (Principales)      |
| [**Creado por USN**](a-usncreated.md)                                            | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | **Top** (Principales)      |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                          | Falso     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | **Top** (Principales)      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los atributos siguientes para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | **Top** (Principales)      |
| [**Common-Name**](a-cn.md)                                                      | Falso     | **Top** (Principales)      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                             | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | **Top** (Principales)      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                         | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | **Top** (Principales)      |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | **Top** (Principales)      |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                   | Falso     | **Top** (Principales)      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | **Top** (Principales)      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | **Top** (Principales)      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | **Top** (Principales)      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | **Top** (Principales)      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | **Top** (Principales)      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | **Top** (Principales)      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | **Top** (Principales)      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | **Top** (Principales)      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | **Top** (Principales)      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | **Top** (Principales)      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | **Top** (Principales)      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | **Top** (Principales)      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                            | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                               | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                   | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | **Top** (Principales)      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | **Top** (Principales)      |
| [**Creado por USN**](a-usncreated.md)                                              | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | **Top** (Principales)      |
| [**Objetos conocidos**](a-wellknownobjects.md)                                 | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | **Top** (Principales)      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Verdadero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdido y encontrado**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                              | Falso     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | **Top** (Principales)      |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | **Top** (Principales)      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falso     | **Top** (Principales)      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | **Top** (Principales)      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | **Top** (Principales)      |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                                  | Falso     | **Top** (Principales)      |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                               | Falso     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                                         | Falso     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                                        | Falso     | **Top** (Principales)      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | **Top** (Principales)      |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | **Top** (Principales)      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                                    | Falso     | **Top** (Principales)      |
| [**Banderas**](a-flags.md)                                                                     | Falso     | **Top** (Principales)      |
| [**Desde entrada**](a-fromentry.md)                                                            | Falso     | **Top** (Principales)      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | **Top** (Principales)      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                                      | Verdadero      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                                            | Falso     | **Top** (Principales)      |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | **Top** (Principales)      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | **Top** (Principales)      |
| [**Se recicla**](a-isrecycled.md)                                                          | Falso     | **Top** (Principales)      |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | Falso     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                                  | Falso     | **Top** (Principales)      |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | **Top** (Principales)      |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                               | Falso     | **Top** (Principales)      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | **Top** (Principales)      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | **Top** (Principales)      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | **Top** (Principales)      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | **Top** (Principales)      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | **Top** (Principales)      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | **Top** (Principales)      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | **Top** (Principales)      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | **Top** (Principales)      |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | **Top** (Principales)      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | **Top** (Principales)      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | **Top** (Principales)      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | **Top** (Principales)      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | **Top** (Principales)      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | **Top** (Principales)      |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | **Top** (Principales)      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | **Top** (Principales)      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | **Top** (Principales)      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | **Top** (Principales)      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | **Top** (Principales)      |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | **Top** (Principales)      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | **Top** (Principales)      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | **Top** (Principales)      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | **Top** (Principales)      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | **Top** (Principales)      |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | **Top** (Principales)      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | **Top** (Principales)      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | **Top** (Principales)      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | **Top** (Principales)      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadero      | **Top** (Principales)      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | **Top** (Principales)      |
| [**Object-Category**](a-objectcategory.md)                                                  | Verdadero      | **Top** (Principales)      |
| [**Object-Class**](a-objectclass.md)                                                        | Verdadero      | **Top** (Principales)      |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | **Top** (Principales)      |
| [**Object-Version**](a-objectversion.md)                                                    | Falso     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | **Top** (Principales)      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | **Top** (Principales)      |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | Falso     | **Top** (Principales)      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | Falso     | **Top** (Principales)      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | **Top** (Principales)      |
| [**Rdn**](a-name.md)                                                                        | Falso     | **Top** (Principales)      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | **Top** (Principales)      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                                           | Falso     | **Top** (Principales)      |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | **Top** (Principales)      |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                               | Falso     | **Top** (Principales)      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | **Top** (Principales)      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | **Top** (Principales)      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | **Top** (Principales)      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | **Top** (Principales)      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | **Top** (Principales)      |
| [**Sub refs**](a-subrefs.md)                                                                | Falso     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | **Top** (Principales)      |
| [**Marcas del sistema**](a-systemflags.md)                                                        | Falso     | **Top** (Principales)      |
| [**USN cambiado**](a-usnchanged.md)                                                          | Falso     | **Top** (Principales)      |
| [**UsN creado**](a-usncreated.md)                                                          | Falso     | **Top** (Principales)      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | **Top** (Principales)      |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | **Top** (Principales)      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | **Top** (Principales)      |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | **Top** (Principales)      |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | Falso     | **Top** (Principales)      |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | Falso     | **Top** (Principales)      |
| [**Cuando se crea**](a-whencreated.md)                                                        | Falso     | **Top** (Principales)      |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                       | Falso     | **Top** (Principales)      |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | **Top** (Principales)      |



 

 





