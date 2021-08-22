---
title: Print-Queue clase
description: Contiene información sobre una cola de impresión.
ms.assetid: 779eb37c-f94e-472a-9551-8a0f72fe0e2b
ms.tgt_platform: multiple
keywords:
- Print-Queue esquema de AD de la clase
- printQueue class AD Schema (Esquema de AD de la clase printQueue)
topic_type:
- apiref
api_name:
- Print-Queue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd05290bcac514607fa44370871d1ba94b5d2b89769d9da20b91c202deea760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753045"
---
# <a name="print-queue-class"></a>Print-Queue clase

Contiene información sobre una cola de impresión.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Print-Queue                          |
| Ldap-Display-Name | Printqueue                           |
| Actualizar privilegios  | Cualquiera puede actualizar este objeto.       |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | bf967aa8-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad organizativa**](c-computer.md)[**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-2000-server-attributes"></a>Windows de servidor 2000

Esta clase contiene los siguientes atributos para Windows 2000 Server:



| Atributo                                                                 | Mandatory | Derivado de                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                               | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                   | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                            | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                         | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                               | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)     | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)              | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)              | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                           | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                  | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de la impresión**](a-printendtime.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                     | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                 | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                            | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                            | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                    | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                    | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Número de impresión**](a-printnumberup.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Orientación de impresión admitida**](a-printorientationssupported.md)      | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Print-Stapling-Supported**](a-printstaplingsupported.md)              | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Estado de impresión**](a-printstatus.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones proxy**](a-proxyaddresses.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                       | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                            | Verdadero      | **Cola de impresión**                                                                          |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                             | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Creado por USN**](a-usncreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                 | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Well-Known-Objects**](a-wellknownobjects.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad**](c-computer.md)organizativa [**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                 | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                              | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                           | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Configuración**](a-msds-settings.md)                                   | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                  | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                             | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                    | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de la impresión**](a-printendtime.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                       | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)     | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Número de impresión**](a-printnumberup.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Orientación de impresión admitida**](a-printorientationssupported.md)        | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                        | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Stapling-Supported**](a-printstaplingsupported.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Estado de impresión**](a-printstatus.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                         | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                              | Verdadero      | **Cola de impresión**                                                                          |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                               | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                   | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad**](c-computer.md)organizativa [**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre común**](a-cn.md)                                                 | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                              | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                           | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Configuración**](a-msds-settings.md)                                   | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                  | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                             | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                               | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                    | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de la impresión**](a-printendtime.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                       | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)     | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Listo para medios de impresión**](a-printmediaready.md)                              | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Number-Up**](a-printnumberup.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Orientaciones de impresión admitidas**](a-printorientationssupported.md)        | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Páginas de impresión por minuto**](a-printpagesperminute.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                        | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Stapling-Supported**](a-printstaplingsupported.md)                | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Estado de impresión**](a-printstatus.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                         | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                              | Verdadero      | **Cola de impresión**                                                                          |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                               | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                   | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad**](c-computer.md)organizativa [**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                          | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Common-Name**](a-cn.md)                                                    | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                      | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                                 | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                              | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Configuración**](a-msds-settings.md)                                      | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)          | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                                | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Intercalación de impresión**](a-printcollate.md)                                        | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                       | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de impresión**](a-printendtime.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                          | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                      | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)        | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                         | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                          | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                         | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                          | Falso     | **Cola de impresión**                                                                          |
| [**Print-Number-Up**](a-printnumberup.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Orientaciones de impresión admitidas**](a-printorientationssupported.md)           | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Páginas de impresión por minuto**](a-printpagesperminute.md)                        | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                      | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la impresión con estapling.**](a-printstaplingsupported.md)                   | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Status**](a-printstatus.md)                                          | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                            | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                                 | Verdadero      | **Cola de impresión**                                                                          |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                  | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Creado por USN**](a-usncreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                      | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad**](c-computer.md)organizativa [**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre común**](a-cn.md)                                                      | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                        | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                                   | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                                | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Configuración**](a-msds-settings.md)                                        | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                       | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)            | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                                  | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                          | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                         | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de la impresión**](a-printendtime.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                            | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                        | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                        | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)          | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                                  | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                           | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Número de impresión**](a-printnumberup.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Orientación de impresión admitida**](a-printorientationssupported.md)             | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                          | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                             | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                        | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la impresión con estapling.**](a-printstaplingsupported.md)                     | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Estado de impresión**](a-printstatus.md)                                            | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                              | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                                   | Verdadero      | **Cola de impresión**                                                                          |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                    | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UsN creado**](a-usncreated.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                        | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                               |
| Subclase de                 | [**Punto de conexión**](c-connectionpoint.md)<br/>                                                                                                             |
| Posibles superiores          | [**Unidad**](c-computer.md)organizativa [**dominio-DNS del contenedor**](c-domaindns.md)[**de equipos**](c-organizationalunit.md) [](c-container.md)                   |
| Clases auxiliares           | \-                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                         |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de recurso**](a-assetnumber.md)                                                        | Falso     | **Cola de impresión**                                                                          |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Bytes por minuto**](a-bytesperminute.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre común**](a-cn.md)                                                                  | Verdadero      | [**Punto de conexión**](c-connectionpoint.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Prioridad predeterminada**](a-defaultpriority.md)                                                | Falso     | **Cola de impresión**                                                                          |
| [**Descripción**](a-description.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del controlador**](a-drivername.md)                                                          | Falso     | **Cola de impresión**                                                                          |
| [**Versión del controlador**](a-driverversion.md)                                                    | Falso     | **Cola de impresión**                                                                          |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Banderas**](a-flags.md)                                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Desde entrada**](a-fromentry.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se elimina**](a-isdeleted.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Se recicla**](a-isrecycled.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Palabras clave**](a-keywords.md)                                                               | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Ubicación**](a-location.md)                                                               | Falso     | **Cola de impresión**                                                                          |
| [**Administrado por**](a-managedby.md)                                                            | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**Objetos administrados**](a-managedobjects.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Configuración**](a-msds-settings.md)                                                    | Falso     | [**Punto de conexión**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Category**](a-objectcategory.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Class**](a-objectclass.md)                                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                          |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Object-Version**](a-objectversion.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                                | Falso     | **Cola de impresión**                                                                          |
| [**Revisión del sistema operativo**](a-operatingsystemhotfix.md)                                   | Falso     | **Cola de impresión**                                                                          |
| [**Operating-System-Service-Pack**](a-operatingsystemservicepack.md)                        | Falso     | **Cola de impresión**                                                                          |
| [**Versión del sistema operativo**](a-operatingsystemversion.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de puerto**](a-portname.md)                                                              | Falso     | **Cola de impresión**                                                                          |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Atributos de impresión**](a-printattributes.md)                                                | Falso     | **Cola de impresión**                                                                          |
| [**Print-Bin-Names**](a-printbinnames.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Collate**](a-printcollate.md)                                                      | Falso     | **Cola de impresión**                                                                          |
| [**Color de impresión**](a-printcolor.md)                                                          | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con dúplex de impresión**](a-printduplexsupported.md)                                     | Falso     | **Cola de impresión**                                                                          |
| [**Hora de finalización de la impresión**](a-printendtime.md)                                                     | Falso     | **Cola de impresión**                                                                          |
| [**Nombre de impresora**](a-printername.md)                                                        | Verdadero      | **Cola de impresión**                                                                          |
| [**Print-Form-Name**](a-printformname.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Print-Keep-Printed-Jobs**](a-printkeepprintedjobs.md)                                    | Falso     | **Cola de impresión**                                                                          |
| [**Idioma de impresión**](a-printlanguage.md)                                                    | Falso     | **Cola de impresión**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                               | Falso     | **Cola de impresión**                                                                          |
| [**Copias máximas de impresión**](a-printmaxcopies.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Se admite la resolución máxima de impresión**](a-printmaxresolutionsupported.md)                      | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-X-Extent**](a-printmaxxextent.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Max-Y-Extent**](a-printmaxyextent.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Media-Ready**](a-printmediaready.md)                                               | Falso     | **Cola de impresión**                                                                          |
| [**Compatible con medios de impresión**](a-printmediasupported.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Memoria de impresión**](a-printmemory.md)                                                        | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-X-Extent**](a-printminxextent.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Min-Y-Extent**](a-printminyextent.md)                                              | Falso     | **Cola de impresión**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                                       | Falso     | **Cola de impresión**                                                                          |
| [**Print-Notify**](a-printnotify.md)                                                        | Falso     | **Cola de impresión**                                                                          |
| [**Número de impresión**](a-printnumberup.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Orientación de impresión admitida**](a-printorientationssupported.md)                         | Falso     | **Cola de impresión**                                                                          |
| [**Propietario de impresión**](a-printowner.md)                                                          | Falso     | **Cola de impresión**                                                                          |
| [**Imprimir páginas por minuto**](a-printpagesperminute.md)                                      | Falso     | **Cola de impresión**                                                                          |
| [**Velocidad de impresión**](a-printrate.md)                                                            | Falso     | **Cola de impresión**                                                                          |
| [**Print-Rate-Unit**](a-printrateunit.md)                                                   | Falso     | **Cola de impresión**                                                                          |
| [**Archivo de separador de impresión**](a-printseparatorfile.md)                                         | Falso     | **Cola de impresión**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Print-Spooling**](a-printspooling.md)                                                    | Falso     | **Cola de impresión**                                                                          |
| [**Print-Stapling-Supported**](a-printstaplingsupported.md)                                 | Falso     | **Cola de impresión**                                                                          |
| [**Hora de inicio de impresión**](a-printstarttime.md)                                                 | Falso     | **Cola de impresión**                                                                          |
| [**Estado de impresión**](a-printstatus.md)                                                        | Falso     | **Cola de impresión**                                                                          |
| [**Priority**](a-priority.md)                                                               | Falso     | **Cola de impresión**                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Informes**](a-directreports.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Revisión**](a-revision.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre del servidor**](a-servername.md)                                                          | Verdadero      | **Cola de impresión**                                                                          |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Nombre corto del servidor**](a-shortservername.md)                                               | Verdadero      | **Cola de impresión**                                                                          |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Sub refs**](a-subrefs.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Marcas del sistema**](a-systemflags.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UNC-Name**](a-uncname.md)                                                                | Verdadero      | **Cola de impresión**                                                                          |
| [**USN cambiado**](a-usnchanged.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**UsN creado**](a-usncreated.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Número de versión**](a-versionnumber.md)                                                    | Verdadero      | **Cola de impresión**                                                                          |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**Cuando se crea**](a-whencreated.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                          |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                          |



 

 





