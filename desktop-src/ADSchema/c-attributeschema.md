---
title: Attribute-Schema (clase)
description: Define un objeto de atributo en el esquema.
ms.assetid: 2338d0ca-b090-4c76-be39-3f54ecb9932d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de clase de Attribute-Schema
- attributeSchema (clase) esquema de AD
topic_type:
- apiref
api_name:
- Attribute-Schema
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62963140d2a12bb37f6bc960bd2cfb23a99a5227
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151368"
---
# <a name="attribute-schema-class"></a>Attribute-Schema (clase)

Define un objeto de atributo en el esquema.



| Entrada | Value |
|-------------------|-----------------------------------------------|
| CN                | Attribute-Schema                              |
| Nombre para mostrar de LDAP | attributeSchema                               |
| Actualizar privilegio  | El administrador del esquema establece este valor. |
| Frecuencia de actualización  | \-                                            |
| Identificador de esquema-GUID    | bf967a80-0de6-11d0-a285-00aa003049e2          |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-2000-server-attributes"></a>Atributos de servidor de Windows 2000

Esta clase contiene los siguientes atributos para el servidor de Windows 2000:



| Atributo                                                                     | Mandatory | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                         | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                 | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                   | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                      | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                       | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                             | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                         | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md) | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                  | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                   | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                         | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                               | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                           | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                           | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                    | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                      | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                         | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                           | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-attributes"></a>Atributos de Windows Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                     | Mandatory | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                         | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                 | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                   | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                      | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                       | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                             | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                         | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md) | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                  | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                           | False     | **Attribute-Schema**                                 |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                   | False     | **Attribute-Schema**                                 |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                   | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                         | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                               | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                           | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                           | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                    | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                      | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                         | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                           | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="adam-attributes"></a>Atributos de ADAM

Esta clase contiene los siguientes atributos para ADAM:



| Atributo                                                                     | Mandatory | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                         | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                 | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                   | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                      | False     | **Attribute-Schema**                                 |
| [**De entrada**](a-fromentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                       | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                             | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                         | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md) | False     | **Attribute-Schema**                                 |
| [**Tiene un único valor**](a-issinglevalued.md)                                  | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Maestro por**](a-masteredby.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                           | False     | **Attribute-Schema**                                 |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                   | False     | **Attribute-Schema**                                 |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                   | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                         | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                               | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                           | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                           | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                    | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                      | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                         | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                           | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-r2-attributes"></a>Atributos de Windows Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                     | Mandatory | Derivado de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                         | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                 | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                   | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                      | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                       | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                             | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                         | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md) | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                  | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                   | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                           | False     | **Attribute-Schema**                                 |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                   | False     | **Attribute-Schema**                                 |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                   | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                         | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                               | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                           | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                           | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                    | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                      | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                         | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                           | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-attributes"></a>Atributos de Windows Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                         |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                          | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                     | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                  | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                               | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                    | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                       | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                        | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                              | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                          | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md)  | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                   | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                 | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                    | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                    | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                            | False     | **Attribute-Schema**                                 |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                    | False     | **Attribute-Schema**                                 |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                       | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                    | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                          | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                     | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                                | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                            | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                            | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                     | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                       | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                          | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                            | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-r2-attributes"></a>Atributos de Windows Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                         |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                            | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                       | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                    | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                 | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                      | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                         | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                                | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                            | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md)    | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Se recicla**](a-isrecycled.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                     | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                   | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                      | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                      | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                              | False     | **Attribute-Schema**                                 |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md) | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                      | False     | **Attribute-Schema**                                 |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                         | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                            | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                       | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                                  | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                              | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                              | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                       | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                         | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                            | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                              | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | False                                  |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valor de ocultación predeterminada        | 1                                      |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**DMD**](c-dmd.md)                   |
| Clases auxiliares           | \-                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2012-attributes"></a>Atributos de Windows Server 2012

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                         |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos**](a-allowedattributes.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR de atributo**](a-attributeid.md)                                                        | True      | **Attribute-Schema**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                                   | False     | **Attribute-Schema**                                 |
| [**Sintaxis de atributo**](a-attributesyntax.md)                                                | True      | **Attribute-Schema**                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre canónico**](a-canonicalname.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                             | False     | **Attribute-Schema**                                 |
| [**Nombre común**](a-cn.md)                                                                  | True      | **Attribute-Schema** [ **Top**](c-top.md)<br/> |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descripción**](a-description.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar**](a-displayname.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Display-Name-printable**](a-displaynameprintable.md)                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DSA-firma**](a-dsasignature.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extended-chars: permitido**](a-extendedcharsallowed.md)                                     | False     | **Attribute-Schema**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas**](a-flags.md)                                                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**De entrada**](a-fromentry.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo de instancia**](a-instancetype.md)                                                      | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-inactivo**](a-isdefunct.md)                                                            | False     | **Attribute-Schema**                                 |
| [**Se elimina**](a-isdeleted.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Efímero**](a-isephemeral.md)                                                        | False     | **Attribute-Schema**                                 |
| [**Is-member-of-DL**](a-memberof.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Is-member-of-parcial-Attribute-set**](a-ismemberofpartialattributeset.md)                | False     | **Attribute-Schema**                                 |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Se recicla**](a-isrecycled.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tiene un único valor**](a-issinglevalued.md)                                                 | True      | **Attribute-Schema**                                 |
| [**Último conocido-primario**](a-lastknownparent.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre para mostrar de LDAP**](a-ldapdisplayname.md)                                               | True      | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de vínculo**](a-linkid.md)                                                                  | False     | **Attribute-Schema**                                 |
| [**Objetos administrados**](a-managedobjects.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**IDENTIFICADOR DE MAPI**](a-mapiid.md)                                                                  | False     | **Attribute-Schema**                                 |
| [**Maestro por**](a-masteredby.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Claim-shares-posibles-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IntId**](a-msds-intid.md)                                                          | False     | **Attribute-Schema**                                 |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-IS-Primary-Computer-para**](a-msds-isprimarycomputerfor.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md)             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Extensiones MS-DS-Schema-Extensions**](a-msds-schema-extensions.md)                                  | False     | **Attribute-Schema**                                 |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-TDO-salida-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-TDO-entrada-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                                     | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Objeto-categoría**](a-objectcategory.md)                                                  | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto**](a-objectclass.md)                                                        | True      | [**Arriba**](c-top.md)<br/>                      |
| [**Object-GUID**](a-objectguid.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Versión del objeto**](a-objectversion.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                                   | False     | **Attribute-Schema**                                 |
| [**OM-sintaxis**](a-omsyntax.md)                                                              | True      | **Attribute-Schema**                                 |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Intervalo: inferior**](a-rangelower.md)                                                          | False     | **Attribute-Schema**                                 |
| [**Intervalo: superior**](a-rangeupper.md)                                                          | False     | **Attribute-Schema**                                 |
| [**RDN**](a-name.md)                                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                                    | False     | [**Arriba**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Informes**](a-directreports.md)                                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes: desde**](a-repsfrom.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Representantes-a**](a-repsto.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Revisión**](a-revision.md)                                                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Schema-Flags-ex**](a-schemaflagsex.md)                                                   | False     | **Attribute-Schema**                                 |
| [**IDENTIFICADOR de esquema-GUID**](a-schemaidguid.md)                                                     | True      | **Attribute-Schema**                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de búsqueda**](a-searchflags.md)                                                        | False     | **Attribute-Schema**                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                                           | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                               | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Referencias secundarias**](a-subrefs.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Marcas de sistema**](a-systemflags.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Solo del sistema**](a-systemonly.md)                                                          | False     | **Attribute-Schema**                                 |
| [**USN: cambiado**](a-usnchanged.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: creado**](a-usncreated.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                                   | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: entre sitios**](a-usnintersite.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                      |
| [**USN: origen**](a-usnsource.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuando se cambia**](a-whenchanged.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**Cuándo se crea**](a-whencreated.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                      |
| [**WWW-página-otro**](a-url.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                      |



 

 





