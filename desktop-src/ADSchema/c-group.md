---
title: Group (clase)
description: Almacena una lista de nombres de usuario. Se usa para aplicar entidades de seguridad en los recursos.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Esquema de AD de clase de grupo
- esquema de AD de clase de grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021913"
---
# <a name="group-class"></a>Group (clase)

Almacena una lista de nombres de usuario. Se usa para aplicar entidades de seguridad en los recursos.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Group (Grupo)                                          |
| Ldap-Display-Name | group                                          |
| Privilegio actualizar  | El administrador del dominio establece este valor. |
| Frecuencia de actualización  | \-                                             |
| Schema-Id-Guid    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Derechos extendidos](#windows-2000-server-extended-rights)
-   [Escrituras validadas](#windows-2000-server-validated-writes)
-   [Conjuntos de propiedades](#windows-2000-server-property-sets)



| Entrada | Value |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                   |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                              |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                     |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)                                       |
| Clases auxiliares           | [**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                        |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows atributos de servidor 2000

Esta clase contiene los siguientes atributos para Windows 2000 Server:



| Atributo                                                                    | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Recuento de administradores**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                    |
| [**Descripción del administrador**](a-admindescription.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Comentario**](a-info.md)                                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Nombre común**](a-cn.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                    |
| [**Create-Time-Stamp**](a-createtimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Nombre de extensión**](a-extensionname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Banderas**](a-flags.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Desde entrada**](a-fromentry.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadero      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Member-Of-DL**](a-memberof.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último elemento primario conocido**](a-lastknownparent.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Administrado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Category**](a-objectcategory.md)                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                            | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de operadores**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles inferiores**](a-possibleinferiors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Informes**](a-directreports.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Librar**](a-rid.md)                                                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sub refs**](a-subrefs.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas del sistema**](a-systemflags.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de teléfono**](a-telephonenumber.md)                                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**User-Cert**](a-usercert.md)                                              | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**USN cambiado**](a-usnchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Creado por USN**](a-usncreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objetos conocidos**](a-wellknownobjects.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se crea**](a-whencreated.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Windows 2000 Server Extended Rights

Esta clase contiene los siguientes derechos extendidos para Windows 2000 Server:



| Nombre común                  |
|------------------------------|
| [**Send-To**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Windows escrituras validadas por el servidor 2000

Esta clase contiene las siguientes escrituras validadas para Windows 2000 Server:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia a sí mismo**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Windows de propiedades del servidor 2000

Esta clase contiene los siguientes conjuntos de propiedades para Windows 2000 Server:



| Nombre común                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Derechos extendidos](#windows-server-2003-extended-rights)
-   [Escrituras validadas](#windows-server-2003-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2003-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                    | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Recuento de administradores**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                    |
| [**Descripción del administrador**](a-admindescription.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Comentario**](a-info.md)                                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Nombre común**](a-cn.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                    |
| [**Crear marca de tiempo**](a-createtimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Nombre de extensión**](a-extensionname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Banderas**](a-flags.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Desde entrada**](a-fromentry.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                    |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadero      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Member-Of-DL**](a-memberof.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Último elemento primario conocido**](a-lastknownparent.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Administrado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                    |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                    |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                    |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembros del grupo NT**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Category**](a-objectcategory.md)                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                            | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de operadores**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                    |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles inferiores**](a-possibleinferiors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Informes**](a-directreports.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Librar**](a-rid.md)                                                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sub refs**](a-subrefs.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas del sistema**](a-systemflags.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de teléfono**](a-telephonenumber.md)                                | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**User-Cert**](a-usercert.md)                                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                         |
| [**USN cambiado**](a-usnchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**UsN creado**](a-usncreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objetos conocidos**](a-wellknownobjects.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se crea**](a-whencreated.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Windows Derechos extendidos de Server 2003

Esta clase contiene los siguientes derechos extendidos para Windows Server 2003:



| Nombre común                  |
|------------------------------|
| [**Send-To**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Escrituras validadas de Server 2003

Esta clase contiene las siguientes escrituras validadas para Windows Server 2003:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia a sí mismo**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Conjuntos de propiedades de Server 2003

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003:



| Nombre común                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



## <a name="adam"></a>Adán

-   [Atributos](#adam-attributes)
-   [Escrituras validadas](#adam-validated-writes)
-   [Conjuntos de propiedades](#adam-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Valor predeterminado de ocultación        | 0                                                                                                                    |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                               |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                      |
| Posibles superiores          | [**Contenedor de unidad organizativa**](c-domaindns.md)de DNS [**de**](c-organizationalunit.md)[**dominio**](c-container.md) |
| Clases auxiliares           | [**Entidad de seguridad**](c-securityprincipal.md) (sistema)                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                         |
| Descriptor de seguridad predeterminado | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Atributos ADAM

Esta clase contiene los atributos siguientes para ADAM:



| Atributo                                                                   | Mandatory | Derivado de                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre común**](a-cn.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Crear marca de tiempo**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                 | Falso     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tipo de grupo**](a-grouptype.md)                                           | Verdadero      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Administrado por**](a-managedby.md)                                           | Falso     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                  | Falso     | **Grupo**                                                                                    |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                           | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                          | Falso     | **Grupo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Credenciales complementarias**](a-supplementalcredentials.md)               | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                       | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Creado por USN**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Escrituras validadas por ADAM

Esta clase contiene las siguientes escrituras validadas para ADAM:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia a sí mismo**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Conjuntos de propiedades ADAM

Esta clase contiene los siguientes conjuntos de propiedades para ADAM:



| Nombre común                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Derechos extendidos](#windows-server-2003-r2-extended-rights)
-   [Escrituras validadas](#windows-server-2003-r2-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2003-r2-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                    | Mandatory | Derivado de                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Recuento de administradores**](a-admincount.md)                                          | Falso     | **Grupo**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Grupo**                                                                                                                          |
| [**Crear marca de tiempo**](a-createtimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                         | Falso     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | Falso     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Banderas**](a-flags.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Desde entrada**](a-fromentry.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                         | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                            | Verdadero      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último elemento primario conocido**](a-lastknownparent.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado por**](a-managedby.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                   | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Category**](a-objectcategory.md)                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                            | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de operadores**](a-operatorcount.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles inferiores**](a-possibleinferiors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Librar**](a-rid.md)                                                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Sub refs**](a-subrefs.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas del sistema**](a-systemflags.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                              | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN cambiado**](a-usnchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Creado por USN**](a-usncreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objetos conocidos**](a-wellknownobjects.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se crea**](a-whencreated.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Derechos extendidos de Server 2003 R2

Esta clase contiene los siguientes derechos extendidos para Windows Server 2003 R2:



| Nombre común                  |
|------------------------------|
| [**Send-To**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Escrituras validadas de Server 2003 R2

Esta clase contiene las siguientes escrituras validadas para Windows Server 2003 R2:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia propia**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Conjuntos de propiedades de Server 2003 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003 R2:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Derechos extendidos](#windows-server-2008-extended-rights)
-   [Escrituras validadas](#windows-server-2008-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2008-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Recuento de administradores**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descripción del administrador**](a-admindescription.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                        | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                             | Falso     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Banderas**](a-flags.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                             | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | Verdadero      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado por**](a-managedby.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de operadores**](a-operatorcount.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Librar**](a-rid.md)                                                             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                     | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                              | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                              | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                    | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                  | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**UsN creado**](a-usncreated.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows Derechos extendidos de Server 2008

Esta clase contiene los siguientes derechos extendidos para Windows Server 2008:



| Nombre común                  |
|------------------------------|
| [**Envío a**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Escrituras validadas de Server 2008

Esta clase contiene las siguientes escrituras validadas para Windows Server 2008:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia propia**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Conjuntos de propiedades de Server 2008

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Derechos extendidos](#windows-server-2008-r2-extended-rights)
-   [Escrituras validadas](#windows-server-2008-r2-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2008-r2-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Recuento de administradores**](a-admincount.md)                                              | Falso     | **Grupo**                                                                                                                          |
| [**Descripción del administrador**](a-admindescription.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                        | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Grupo**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                             | Falso     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                      | Falso     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Banderas**](a-flags.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                             | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | Verdadero      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado por**](a-managedby.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falso     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de operadores**](a-operatorcount.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Librar**](a-rid.md)                                                             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                     | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                              | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                              | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                    | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                  | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**UsN creado**](a-usncreated.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Derechos extendidos de Server 2008 R2

Esta clase contiene los siguientes derechos extendidos para Windows Server 2008 R2:



| Nombre común                  |
|------------------------------|
| [**Envío a**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Escrituras validadas de Server 2008 R2

Esta clase contiene las siguientes escrituras validadas para Windows Server 2008 R2:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia propia**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Conjuntos de propiedades de Server 2008 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008 R2:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Derechos extendidos](#windows-server-2012-extended-rights)
-   [Escrituras validadas](#windows-server-2012-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2012-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor predeterminado de ocultación        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Recuento de administradores**](a-admincount.md)                                                          | Falso     | **Grupo**                                                                                                                          |
| [**Descripción del administrador**](a-admindescription.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                                   | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                                  | Verdadero      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                                       | Falso     | **Grupo**                                                                                                                          |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                                  | Falso     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                                           | Falso     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Banderas**](a-flags.md)                                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Desde entrada**](a-fromentry.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                                           | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**Pertenencia a grupos-SAM**](a-groupmembershipsam.md)                                         | Falso     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                            | Verdadero      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se recicla**](a-isrecycled.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado por**](a-managedby.md)                                                            | Falso     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                                   | Falso     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                                | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                                          | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-GeoCoordinates-Altitude**](a-msds-geocoordinatesaltitude.md)                       | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                       | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                     | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                               | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Primary-Computer**](a-msds-primarycomputer.md)                                     | Falso     | **Grupo**                                                                                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                                       | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                            | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                                        | Falso     | **Grupo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembros del grupo NT**](a-ntgroupmembers.md)                                                 | Falso     | **Grupo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Category**](a-objectcategory.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Class**](a-objectclass.md)                                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                            | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Object-Version**](a-objectversion.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de operadores**](a-operatorcount.md)                                                    | Falso     | **Grupo**                                                                                                                          |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                                           | Falso     | **Grupo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Librar**](a-rid.md)                                                                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                                 | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                                 | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                                          | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Sub refs**](a-subrefs.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                                | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas del sistema**](a-systemflags.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                                | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                                        | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md)                 | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)                         | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-Cert**](a-usercert.md)                                                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                     | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN cambiado**](a-usnchanged.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**UsN creado**](a-usncreated.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se crea**](a-whencreated.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                                       | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Derechos extendidos

Esta clase contiene los siguientes derechos extendidos para Windows Server 2012:



| Nombre común                  |
|------------------------------|
| [**Envío a**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Escrituras validadas

Esta clase contiene las siguientes escrituras validadas para Windows Server 2012:



| Nombre común                                  |
|----------------------------------------------|
| [**Pertenencia propia**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Conjuntos de propiedades

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2012:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



 

 





