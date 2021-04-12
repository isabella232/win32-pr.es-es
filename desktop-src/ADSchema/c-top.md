---
title: Clase principal
description: La clase de nivel superior de la que se derivan todas las clases.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de clase principal
- Esquema de AD de clase principal
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151303"
---
# <a name="top-class"></a>Clase principal

La clase de nivel superior de la que se derivan todas las clases.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Superior                                  |
| Nombre para mostrar de LDAP | top                                  |
| Actualizar privilegio  | Administrador de esquema                 |
| Frecuencia de actualización  | \-                                   |
| Identificador de esquema-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Atributos de servidor de Windows 2000

Esta clase contiene los siguientes atributos para el servidor de Windows 2000:



| Atributo                                                                 | Mandatory | Derivado de |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                           | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                         | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)      | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                    | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md) | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)             | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                 | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                               | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                            | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                      | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                     | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                  | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                   | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)               | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                 | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                  | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                         | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                   | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                         | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                     | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                        | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                            | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                               | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                       | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                            | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                  | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                              | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                               | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                     | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                       | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                 | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)               | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md) | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                    | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                         | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                        | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                               | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                     | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                 | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                        | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                           | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                               | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                            | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                        | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                        | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)            | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                  | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                             | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                     | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                       | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                       | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                   | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                         | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                           | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                          | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                     | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                     | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                           | False     | **Top** (Principales)      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Atributos de Windows Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                             | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                 | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                    | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                    | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                           | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                          | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                         | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | **Top** (Principales)      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | **Top** (Principales)      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top** (Principales)      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top** (Principales)      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top** (Principales)      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                         | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                       | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                          | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                 | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                         | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                           | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                             | False     | **Top** (Principales)      |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Value |
|-----------------------------|------------------------------------------|
| System-Only                 | True                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Valor de ocultación predeterminada        | 1                                        |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>   |
| Subclase de                 | **Top** (Principales)<br/>                       |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md) |
| Clases auxiliares           | \-                                       |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                             |
| Descriptor de seguridad predeterminado | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Atributos de ADAM

Esta clase contiene los siguientes atributos para ADAM:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                             | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                 | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                           | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                         | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | **Top** (Principales)      |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                         | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                       | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                 | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                         | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                           | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                             | False     | **Top** (Principales)      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Atributos de Windows Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                             | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                 | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                        | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                    | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                    | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                           | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                           | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                          | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                         | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | **Top** (Principales)      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | **Top** (Principales)      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | **Top** (Principales)      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | **Top** (Principales)      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | **Top** (Principales)      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | **Top** (Principales)      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | **Top** (Principales)      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | **Top** (Principales)      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                         | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                       | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                          | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                 | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                              | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                         | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                           | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                             | False     | **Top** (Principales)      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Atributos de Windows Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                                | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                              | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)           | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                         | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)      | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                  | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                      | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                    | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                 | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                           | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                          | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                       | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                        | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                    | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                      | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                       | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                              | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                     | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                        | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                              | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                          | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                             | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                                 | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                    | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                            | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                 | False     | **Top** (Principales)      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | **Top** (Principales)      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | False     | **Top** (Principales)      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | **Top** (Principales)      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | False     | **Top** (Principales)      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | **Top** (Principales)      |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)             | False     | **Top** (Principales)      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                 | False     | **Top** (Principales)      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                          | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)       | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | **Top** (Principales)      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | **Top** (Principales)      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                         | False     | **Top** (Principales)      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | **Top** (Principales)      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | **Top** (Principales)      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                           | False     | **Top** (Principales)      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                 | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)         | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                 | False     | **Top** (Principales)      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                             | False     | **Top** (Principales)      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                        | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | **Top** (Principales)      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | **Top** (Principales)      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                       | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                   | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                    | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                          | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                            | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                      | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)      | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                         | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                              | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                             | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                     | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                          | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                      | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                             | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                                | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                    | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                 | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                             | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                             | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                 | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                       | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                     | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                                  | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                          | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                            | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                            | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                     | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                        | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                              | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                               | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                          | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                          | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                                | False     | **Top** (Principales)      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Atributos de Windows Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                                  | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                                | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)             | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                           | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)        | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                    | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                        | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                      | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                   | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                             | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                         | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                          | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                      | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                         | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                                | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                       | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                                | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                            | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                               | False     | **Top** (Principales)      |
| [**Se recicla**](a-isrecycled.md)                                              | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                                   | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                              | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                   | False     | **Top** (Principales)      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | **Top** (Principales)      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | **Top** (Principales)      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | **Top** (Principales)      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | False     | **Top** (Principales)      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | **Top** (Principales)      |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | **Top** (Principales)      |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | **Top** (Principales)      |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                | False     | **Top** (Principales)      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                     | False     | **Top** (Principales)      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)               | False     | **Top** (Principales)      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md) | False     | **Top** (Principales)      |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)   | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                   | False     | **Top** (Principales)      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                            | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)         | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | **Top** (Principales)      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | **Top** (Principales)      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                           | False     | **Top** (Principales)      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | **Top** (Principales)      |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | **Top** (Principales)      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                             | False     | **Top** (Principales)      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                   | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)           | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                               | False     | **Top** (Principales)      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                          | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | **Top** (Principales)      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | **Top** (Principales)      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                         | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                     | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                      | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                            | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                              | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                        | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)        | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                           | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                               | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                       | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                            | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                        | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                               | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                                  | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                      | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                   | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                               | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                               | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                   | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                         | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                       | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                                    | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                            | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                              | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                              | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                       | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                          | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                                | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                  | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                            | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                            | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                                  | False     | **Top** (Principales)      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valor de ocultación predeterminada        | 1                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | **Top** (Principales)<br/>                                                                           |
| Posibles superiores          | [**Perdidos y encontrados**](c-lostandfound.md)                                                     |
| Clases auxiliares           | \-                                                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Atributos de Windows Server 2012

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Admin: Descripción**](a-admindescription.md)                                              | False     | **Top** (Principales)      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | **Top** (Principales)      |
| [**Permitido: atributos**](a-allowedattributes.md)                                            | False     | **Top** (Principales)      |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)                         | False     | **Top** (Principales)      |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                                       | False     | **Top** (Principales)      |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)                    | False     | **Top** (Principales)      |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                                | False     | **Top** (Principales)      |
| [**Nombre canónico**](a-canonicalname.md)                                                    | False     | **Top** (Principales)      |
| [**Nombre común**](a-cn.md)                                                                  | False     | **Top** (Principales)      |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                               | False     | **Top** (Principales)      |
| [**Descripción**](a-description.md)                                                         | False     | **Top** (Principales)      |
| [**Nombre para mostrar**](a-displayname.md)                                                        | False     | **Top** (Principales)      |
| [**Display-Name-printable**](a-displaynameprintable.md)                                     | False     | **Top** (Principales)      |
| [**DSA-firma**](a-dsasignature.md)                                                      | False     | **Top** (Principales)      |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                                  | False     | **Top** (Principales)      |
| [**Nombre de extensión**](a-extensionname.md)                                                    | False     | **Top** (Principales)      |
| [**Marcas**](a-flags.md)                                                                     | False     | **Top** (Principales)      |
| [**De entrada**](a-fromentry.md)                                                            | False     | **Top** (Principales)      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | **Top** (Principales)      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | **Top** (Principales)      |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                                   | False     | **Top** (Principales)      |
| [**Tipo de instancia**](a-instancetype.md)                                                      | True      | **Top** (Principales)      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | **Top** (Principales)      |
| [**Se elimina**](a-isdeleted.md)                                                            | False     | **Top** (Principales)      |
| [**Is-member-of-DL**](a-memberof.md)                                                        | False     | **Top** (Principales)      |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                                           | False     | **Top** (Principales)      |
| [**Se recicla**](a-isrecycled.md)                                                          | False     | **Top** (Principales)      |
| [**Último conocido-primario**](a-lastknownparent.md)                                               | False     | **Top** (Principales)      |
| [**Objetos administrados**](a-managedobjects.md)                                                  | False     | **Top** (Principales)      |
| [**Maestro por**](a-masteredby.md)                                                          | False     | **Top** (Principales)      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                               | False     | **Top** (Principales)      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | **Top** (Principales)      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | **Top** (Principales)      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | **Top** (Principales)      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | **Top** (Principales)      |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | False     | **Top** (Principales)      |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | **Top** (Principales)      |
| [**MS-DS-Claim-shares-posibles-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | **Top** (Principales)      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | **Top** (Principales)      |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | **Top** (Principales)      |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | **Top** (Principales)      |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                            | False     | **Top** (Principales)      |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                                 | False     | **Top** (Principales)      |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)                           | False     | **Top** (Principales)      |
| [**MS-DS-IS-Primary-Computer-para**](a-msds-isprimarycomputerfor.md)                         | False     | **Top** (Principales)      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | **Top** (Principales)      |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                                          | False     | **Top** (Principales)      |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md)             | False     | **Top** (Principales)      |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)               | False     | **Top** (Principales)      |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                               | False     | **Top** (Principales)      |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | False     | **Top** (Principales)      |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                                        | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)                     | False     | **Top** (Principales)      |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | **Top** (Principales)      |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | **Top** (Principales)      |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                                       | False     | **Top** (Principales)      |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | **Top** (Principales)      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | **Top** (Principales)      |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | False     | **Top** (Principales)      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | **Top** (Principales)      |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                                         | False     | **Top** (Principales)      |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                               | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | False     | **Top** (Principales)      |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                               | False     | **Top** (Principales)      |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                                           | False     | **Top** (Principales)      |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                                      | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | False     | **Top** (Principales)      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | **Top** (Principales)      |
| [**MS-DS-TDO-salida-BL**](a-msds-tdoegressbl.md)                                            | False     | **Top** (Principales)      |
| [**MS-DS-TDO-entrada-BL**](a-msds-tdoingressbl.md)                                          | False     | **Top** (Principales)      |
| [**MS-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | **Top** (Principales)      |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | **Top** (Principales)      |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | False     | **Top** (Principales)      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | **Top** (Principales)      |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | False     | **Top** (Principales)      |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                                     | True      | **Top** (Principales)      |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                                 | False     | **Top** (Principales)      |
| [**Objeto-categoría**](a-objectcategory.md)                                                  | True      | **Top** (Principales)      |
| [**Clase de objeto**](a-objectclass.md)                                                        | True      | **Top** (Principales)      |
| [**Object-GUID**](a-objectguid.md)                                                          | False     | **Top** (Principales)      |
| [**Versión del objeto**](a-objectversion.md)                                                    | False     | **Top** (Principales)      |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | False     | **Top** (Principales)      |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)                    | False     | **Top** (Principales)      |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                                       | False     | **Top** (Principales)      |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                            | False     | **Top** (Principales)      |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                                           | False     | **Top** (Principales)      |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | False     | **Top** (Principales)      |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                                   | False     | **Top** (Principales)      |
| [**RDN**](a-name.md)                                                                        | False     | **Top** (Principales)      |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                                    | False     | **Top** (Principales)      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | **Top** (Principales)      |
| [**Informes**](a-directreports.md)                                                           | False     | **Top** (Principales)      |
| [**Representantes: desde**](a-repsfrom.md)                                                              | False     | **Top** (Principales)      |
| [**Representantes-a**](a-repsto.md)                                                                  | False     | **Top** (Principales)      |
| [**Revisión**](a-revision.md)                                                               | False     | **Top** (Principales)      |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                                           | False     | **Top** (Principales)      |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                                           | False     | **Top** (Principales)      |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                               | False     | **Top** (Principales)      |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                                     | False     | **Top** (Principales)      |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                                   | False     | **Top** (Principales)      |
| [**Referencias secundarias**](a-subrefs.md)                                                                | False     | **Top** (Principales)      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | **Top** (Principales)      |
| [**Marcas de sistema**](a-systemflags.md)                                                        | False     | **Top** (Principales)      |
| [**USN: cambiado**](a-usnchanged.md)                                                          | False     | **Top** (Principales)      |
| [**USN: creado**](a-usncreated.md)                                                          | False     | **Top** (Principales)      |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                                   | False     | **Top** (Principales)      |
| [**USN: entre sitios**](a-usnintersite.md)                                                      | False     | **Top** (Principales)      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | False     | **Top** (Principales)      |
| [**USN: origen**](a-usnsource.md)                                                            | False     | **Top** (Principales)      |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                              | False     | **Top** (Principales)      |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | False     | **Top** (Principales)      |
| [**Cuando se cambia**](a-whenchanged.md)                                                        | False     | **Top** (Principales)      |
| [**Cuándo se crea**](a-whencreated.md)                                                        | False     | **Top** (Principales)      |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                       | False     | **Top** (Principales)      |
| [**WWW-página-otro**](a-url.md)                                                              | False     | **Top** (Principales)      |



 

 





