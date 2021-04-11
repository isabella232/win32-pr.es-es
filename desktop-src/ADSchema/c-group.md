---
title: Group (clase)
description: Almacena una lista de nombres de usuario. Se usa para aplicar entidades de seguridad en los recursos.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Esquema de la clase de grupo AD
- Esquema de la clase de grupo AD
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618adb97220f4cc1b1e4af7f42fd043c7bb1e6c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151358"
---
# <a name="group-class"></a>Group (clase)

Almacena una lista de nombres de usuario. Se usa para aplicar entidades de seguridad en los recursos.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Grupo                                          |
| Nombre para mostrar de LDAP | group                                          |
| Actualizar privilegio  | El administrador del dominio establece este valor. |
| Frecuencia de actualización  | \-                                             |
| Identificador de esquema-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Derechos extendidos](#windows-2000-server-extended-rights)
-   [Escrituras validadas](#windows-2000-server-validated-writes)
-   [Conjuntos de propiedades](#windows-2000-server-property-sets)



| Entrada | Value |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                   |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                              |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                     |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)integrada de dominio DNS-[**contenedor**](c-container.md) [**de dominio**](c-builtindomain.md)                                       |
| Clases auxiliares           | [**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                        |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                        |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; ESTÉ |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Atributos de servidor de Windows 2000

Esta clase contiene los siguientes atributos para el servidor de Windows 2000:



| Atributo                                                                    | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Administrador: recuento**](a-admincount.md)                                          | False     | **Grupo**                                                                                    |
| [**Admin: Descripción**](a-admindescription.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos**](a-allowedattributes.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                   | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre canónico**](a-canonicalname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Comentario**](a-info.md)                                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Nombre común**](a-cn.md)                                                  | True      | [**Arriba**](c-top.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>         |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                       | False     | **Grupo**                                                                                    |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | False     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Display-Name-printable**](a-displaynameprintable.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | False     | **Grupo**                                                                                    |
| [**Nombre de extensión**](a-extensionname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Marcas**](a-flags.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | False     | **Grupo**                                                                                    |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                         | False     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último conocido-primario**](a-lastknownparent.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Administrado: por**](a-managedby.md)                                            | False     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Maestro por**](a-masteredby.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                   | False     | **Grupo**                                                                                    |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | False     | **Grupo**                                                                                    |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                 | False     | **Grupo**                                                                                    |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                     | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto-categoría**](a-objectcategory.md)                                  | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto**](a-objectclass.md)                                        | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-GUID**](a-objectguid.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto: SID**](a-objectsid.md)                                            | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Versión del objeto**](a-objectversion.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Operador-recuento**](a-operatorcount.md)                                    | False     | **Grupo**                                                                                    |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles: inferiores**](a-possibleinferiors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Token de grupo principal**](a-primarygrouptoken.md)                           | False     | **Grupo**                                                                                    |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Informes**](a-directreports.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes: desde**](a-repsfrom.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes-a**](a-repsto.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Libra**](a-rid.md)                                                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                 | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                 | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Historial de SID**](a-sidhistory.md)                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Referencias secundarias**](a-subrefs.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas de sistema**](a-systemflags.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de teléfono**](a-telephonenumber.md)                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Certificado de usuario**](a-usercert.md)                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**USN: cambiado**](a-usnchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: creado**](a-usncreated.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: entre sitios**](a-usnintersite.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: origen**](a-usnsource.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Well-Known-Objects**](a-wellknownobjects.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se cambia**](a-whenchanged.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se crea**](a-whencreated.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-página-otro**](a-url.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Derechos extendidos del servidor de Windows 2000

Esta clase contiene los siguientes derechos extendidos para Windows 2000 Server:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Escrituras validadas del servidor de Windows 2000

Esta clase contiene las siguientes escrituras validadas para el servidor de Windows 2000:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Conjuntos de propiedades de servidor de Windows 2000

Esta clase contiene los siguientes conjuntos de propiedades para el servidor de Windows 2000:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Derechos extendidos](#windows-server-2003-extended-rights)
-   [Escrituras validadas](#windows-server-2003-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2003-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)[**integrada de**](c-builtindomain.md)dominio DNS-[**contenedor**](c-container.md)de dominio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                                                                                                                                     |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Atributos de Windows Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                    | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Administrador: recuento**](a-admincount.md)                                          | False     | **Grupo**                                                                                    |
| [**Admin: Descripción**](a-admindescription.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos**](a-allowedattributes.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                   | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre canónico**](a-canonicalname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Comentario**](a-info.md)                                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Nombre común**](a-cn.md)                                                  | True      | [**Arriba**](c-top.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>         |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                       | False     | **Grupo**                                                                                    |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | False     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Display-Name-printable**](a-displaynameprintable.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | False     | **Grupo**                                                                                    |
| [**Nombre de extensión**](a-extensionname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Marcas**](a-flags.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Atributos de grupo**](a-groupattributes.md)                                | False     | **Grupo**                                                                                    |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                         | False     | **Grupo**                                                                                    |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Último conocido-primario**](a-lastknownparent.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Administrado: por**](a-managedby.md)                                            | False     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Maestro por**](a-masteredby.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                   | False     | **Grupo**                                                                                    |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | False     | **Grupo**                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-no miembros**](a-msds-nonmembers.md)                               | False     | **Grupo**                                                                                    |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | False     | **Grupo**                                                                                    |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                 | False     | **Grupo**                                                                                    |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                     | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto-categoría**](a-objectcategory.md)                                  | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto**](a-objectclass.md)                                        | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-GUID**](a-objectguid.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto: SID**](a-objectsid.md)                                            | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Versión del objeto**](a-objectversion.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Operador-recuento**](a-operatorcount.md)                                    | False     | **Grupo**                                                                                    |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles: inferiores**](a-possibleinferiors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Token de grupo principal**](a-primarygrouptoken.md)                           | False     | **Grupo**                                                                                    |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Informes**](a-directreports.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes: desde**](a-repsfrom.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes-a**](a-repsto.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Libra**](a-rid.md)                                                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                 | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                 | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Historial de SID**](a-sidhistory.md)                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Referencias secundarias**](a-subrefs.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas de sistema**](a-systemflags.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Número de teléfono**](a-telephonenumber.md)                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Grupos de tokens**](a-tokengroups.md)                                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Certificado de usuario**](a-usercert.md)                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |
| [**USN: cambiado**](a-usnchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: creado**](a-usncreated.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: entre sitios**](a-usnintersite.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: origen**](a-usnsource.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Well-Known-Objects**](a-wellknownobjects.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se cambia**](a-whenchanged.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se crea**](a-whencreated.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-página-otro**](a-url.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Derechos extendidos de Windows Server 2003

Esta clase contiene los siguientes derechos extendidos para Windows Server 2003:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Escrituras validadas de Windows Server 2003

Esta clase contiene las siguientes escrituras validadas para Windows Server 2003:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Conjuntos de propiedades de Windows Server 2003

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)
-   [Escrituras validadas](#adam-validated-writes)
-   [Conjuntos de propiedades](#adam-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Valor de ocultación predeterminada        | 0                                                                                                                    |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                               |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                      |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**contenedor**](c-container.md) [**de unidades organizativas de**](c-organizationalunit.md)DNS |
| Clases auxiliares           | [**Seguridad: entidad de seguridad**](c-securityprincipal.md) (sistema)                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                         |
| Descriptor de seguridad predeterminado | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Atributos de ADAM

Esta clase contiene los siguientes atributos para ADAM:



| Atributo                                                                   | Mandatory | Derivado de                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Admin: Descripción**](a-admindescription.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre común**](a-cn.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Perfil de escritorio**](a-desktopprofile.md)                                 | False     | **Grupo**                                                                                    |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tipo de grupo**](a-grouptype.md)                                           | True      | **Grupo**                                                                                    |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Administrado: por**](a-managedby.md)                                           | False     | **Grupo**                                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Maestro por**](a-masteredby.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Miembro**](a-member.md)                                                  | False     | **Grupo**                                                                                    |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-GUID**](a-objectguid.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto: SID**](a-objectsid.md)                                           | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Token de grupo principal**](a-primarygrouptoken.md)                          | False     | **Grupo**                                                                                    |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes-a**](a-repsto.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)               | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                       | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: creado**](a-usncreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: origen**](a-usnsource.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-página-otro**](a-url.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Escrituras validadas por ADAM

Esta clase contiene las siguientes escrituras validadas para ADAM:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Conjuntos de propiedades de ADAM

Esta clase contiene los siguientes conjuntos de propiedades para ADAM:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Derechos extendidos](#windows-server-2003-r2-extended-rights)
-   [Escrituras validadas](#windows-server-2003-r2-validated-writes)
-   [Conjuntos de propiedades](#windows-server-2003-r2-property-sets)



| Entrada | Value |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)[**integrada de**](c-builtindomain.md)dominio DNS-[**contenedor**](c-container.md)de dominio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Atributos de Windows Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                    | Mandatory | Derivado de                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Administrador: recuento**](a-admincount.md)                                          | False     | **Grupo**                                                                                                                          |
| [**Admin: Descripción**](a-admindescription.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos**](a-allowedattributes.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                   | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre canónico**](a-canonicalname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                  | True      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                       | False     | **Grupo**                                                                                                                          |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                         | False     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                  | False     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-printable**](a-displaynameprintable.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                           | False     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Marcas**](a-flags.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                | False     | **Grupo**                                                                                                                          |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                         | False     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                            | True      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último conocido-primario**](a-lastknownparent.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado: por**](a-managedby.md)                                            | False     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Maestro por**](a-masteredby.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                   | False     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | False     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-no miembros**](a-msds-nonmembers.md)                               | False     | **Grupo**                                                                                                                          |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nombre**](a-mssfu30name.md)                                       | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-dominio**](a-mssfu30nisdomain.md)                            | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                        | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                           | False     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                 | False     | **Grupo**                                                                                                                          |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                     | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoría**](a-objectcategory.md)                                  | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto**](a-objectclass.md)                                        | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-GUID**](a-objectguid.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto: SID**](a-objectsid.md)                                            | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Versión del objeto**](a-objectversion.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Operador-recuento**](a-operatorcount.md)                                    | False     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles: inferiores**](a-possibleinferiors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo principal**](a-primarygrouptoken.md)                           | False     | **Grupo**                                                                                                                          |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes: desde**](a-repsfrom.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes-a**](a-repsto.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Libra**](a-rid.md)                                                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                 | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                 | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Historial de SID**](a-sidhistory.md)                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Referencias secundarias**](a-subrefs.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas de sistema**](a-systemflags.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md) | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario**](a-usercert.md)                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                      | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN: cambiado**](a-usnchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: creado**](a-usncreated.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: entre sitios**](a-usnintersite.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: origen**](a-usnsource.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se cambia**](a-whenchanged.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se crea**](a-whencreated.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Página principal**](a-wwwhomepage.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-otro**](a-url.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Derechos extendidos de Windows Server 2003 R2

Esta clase contiene los siguientes derechos extendidos para Windows Server 2003 R2:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Escrituras validadas de Windows Server 2003 R2

Esta clase contiene las siguientes escrituras validadas para Windows Server 2003 R2:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Conjuntos de propiedades de Windows Server 2003 R2

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
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)[**integrada de**](c-builtindomain.md)dominio DNS-[**contenedor**](c-container.md)de dominio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Atributos de Windows Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Administrador: recuento**](a-admincount.md)                                              | False     | **Grupo**                                                                                                                          |
| [**Admin: Descripción**](a-admindescription.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos**](a-allowedattributes.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                       | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre canónico**](a-canonicalname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                      | True      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                           | False     | **Grupo**                                                                                                                          |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                             | False     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                      | False     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-printable**](a-displaynameprintable.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | False     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Marcas**](a-flags.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | False     | **Grupo**                                                                                                                          |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                             | False     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | True      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último conocido-primario**](a-lastknownparent.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado: por**](a-managedby.md)                                                | False     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Maestro por**](a-masteredby.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                       | False     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                    | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                   | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BIZ-Rule-path**](a-msds-azlastimportedbizrulepath.md) | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | False     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-no miembros**](a-msds-nonmembers.md)                                   | False     | **Grupo**                                                                                                                          |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nombre**](a-mssfu30name.md)                                           | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-dominio**](a-mssfu30nisdomain.md)                                | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                               | False     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                     | False     | **Grupo**                                                                                                                          |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                         | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoría**](a-objectcategory.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto**](a-objectclass.md)                                            | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-GUID**](a-objectguid.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto: SID**](a-objectsid.md)                                                | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Versión del objeto**](a-objectversion.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Operador-recuento**](a-operatorcount.md)                                        | False     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo principal**](a-primarygrouptoken.md)                               | False     | **Grupo**                                                                                                                          |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes: desde**](a-repsfrom.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes-a**](a-repsto.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Libra**](a-rid.md)                                                             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                     | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                     | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                              | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Historial de SID**](a-sidhistory.md)                                              | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Referencias secundarias**](a-subrefs.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                    | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas de sistema**](a-systemflags.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md)     | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario**](a-usercert.md)                                                  | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                          | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN: cambiado**](a-usnchanged.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: creado**](a-usncreated.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: entre sitios**](a-usnintersite.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: origen**](a-usnsource.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se cambia**](a-whenchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se crea**](a-whencreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-otro**](a-url.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Derechos extendidos de Windows Server 2008

Esta clase contiene los siguientes derechos extendidos para Windows Server 2008:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Escrituras validadas de Windows Server 2008

Esta clase contiene las siguientes escrituras validadas para Windows Server 2008:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Conjuntos de propiedades de Windows Server 2008

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
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)[**integrada de**](c-builtindomain.md)dominio DNS-[**contenedor**](c-container.md)de dominio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Atributos de Windows Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Administrador: recuento**](a-admincount.md)                                              | False     | **Grupo**                                                                                                                          |
| [**Admin: Descripción**](a-admindescription.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos**](a-allowedattributes.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                       | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre canónico**](a-canonicalname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                      | True      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                           | False     | **Grupo**                                                                                                                          |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                             | False     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                      | False     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-printable**](a-displaynameprintable.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | False     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Marcas**](a-flags.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                    | False     | **Grupo**                                                                                                                          |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                             | False     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                | True      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se recicla**](a-isrecycled.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último conocido-primario**](a-lastknownparent.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado: por**](a-managedby.md)                                                | False     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Maestro por**](a-masteredby.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                       | False     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                    | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                   | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BIZ-Rule-path**](a-msds-azlastimportedbizrulepath.md) | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | False     | **Grupo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-no miembros**](a-msds-nonmembers.md)                                   | False     | **Grupo**                                                                                                                          |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nombre**](a-mssfu30name.md)                                           | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-dominio**](a-mssfu30nisdomain.md)                                | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                               | False     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                     | False     | **Grupo**                                                                                                                          |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                         | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoría**](a-objectcategory.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto**](a-objectclass.md)                                            | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-GUID**](a-objectguid.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto: SID**](a-objectsid.md)                                                | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Versión del objeto**](a-objectversion.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Operador-recuento**](a-operatorcount.md)                                        | False     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo principal**](a-primarygrouptoken.md)                               | False     | **Grupo**                                                                                                                          |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes: desde**](a-repsfrom.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes-a**](a-repsto.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Libra**](a-rid.md)                                                             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                     | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                     | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                              | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Historial de SID**](a-sidhistory.md)                                              | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Referencias secundarias**](a-subrefs.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                    | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas de sistema**](a-systemflags.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                            | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md)     | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)             | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario**](a-usercert.md)                                                  | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                          | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN: cambiado**](a-usnchanged.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: creado**](a-usncreated.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: entre sitios**](a-usnintersite.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: origen**](a-usnsource.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se cambia**](a-whenchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se crea**](a-whencreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-otro**](a-url.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Derechos extendidos de Windows Server 2008 R2

Esta clase contiene los siguientes derechos extendidos para Windows Server 2008 R2:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Escrituras validadas de Windows Server 2008 R2

Esta clase contiene las siguientes escrituras validadas para Windows Server 2008 R2:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Conjuntos de propiedades de Windows Server 2008 R2

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
| System-Only                 | False                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valor de ocultación predeterminada        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Posibles superiores          | [**Dominio:**](c-domaindns.md)[**unidad organizativa**](c-organizationalunit.md)[**integrada de**](c-builtindomain.md)dominio DNS-[**contenedor**](c-container.md)de dominio [**MS-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Clases auxiliares           | [**posixGroup**](c-posixgroup.md)[**Security-principal**](c-securityprincipal.md) (sistema)[**-destinatario de correo**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11d0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Atributos de Windows Server 2012

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre de cuenta-historial**](a-accountnamehistory.md)                                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Administrador: recuento**](a-admincount.md)                                                          | False     | **Grupo**                                                                                                                          |
| [**Admin: Descripción**](a-admindescription.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos**](a-allowedattributes.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Alt-seguridad-identidades**](a-altsecurityidentities.md)                                   | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre canónico**](a-canonicalname.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Comentario**](a-info.md)                                                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Nombre común**](a-cn.md)                                                                  | True      | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> |
| [**Derechos de acceso de control**](a-controlaccessrights.md)                                       | False     | **Grupo**                                                                                                                          |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Descripción**](a-description.md)                                                         | False     | [**Arriba**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Perfil de escritorio**](a-desktopprofile.md)                                                  | False     | **Grupo**                                                                                                                          |
| [**Nombre para mostrar**](a-displayname.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-printable**](a-displaynameprintable.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones de correo electrónico**](a-mail.md)                                                           | False     | **Grupo**                                                                                                                          |
| [**Nombre de extensión**](a-extensionname.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Marcas**](a-flags.md)                                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**De entrada**](a-fromentry.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Atributos de grupo**](a-groupattributes.md)                                                | False     | **Grupo**                                                                                                                          |
| [**Grupo-pertenencia-SAM**](a-groupmembershipsam.md)                                         | False     | **Grupo**                                                                                                                          |
| [**Tipo de grupo**](a-grouptype.md)                                                            | True      | **Grupo**                                                                                                                          |
| [**Tipo de instancia**](a-instancetype.md)                                                      | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se elimina**](a-isdeleted.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Se recicla**](a-isrecycled.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Último conocido-primario**](a-lastknownparent.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Administrado: por**](a-managedby.md)                                                            | False     | **Grupo**                                                                                                                          |
| [**Objetos administrados**](a-managedobjects.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Maestro por**](a-masteredby.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro**](a-member.md)                                                                   | False     | **Grupo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule**](a-msds-azbizrule.md)                                                | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-BIZ-Rule-Language**](a-msds-azbizrulelanguage.md)                               | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                                        | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BIZ-Rule-path**](a-msds-azlastimportedbizrulepath.md)             | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                            | False     | **Grupo**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | False     | **Grupo**                                                                                                                          |
| [**MS-DS-Claim-shares-posibles-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-geocoordinations-altitud**](a-msds-geocoordinatesaltitude.md)                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-geocoordinations-latitud**](a-msds-geocoordinateslatitude.md)                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-geocoordinations-longitud**](a-msds-geocoordinateslongitude.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-IS-Primary-Computer-para**](a-msds-isprimarycomputerfor.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-no miembros**](a-msds-nonmembers.md)                                               | False     | **Grupo**                                                                                                                          |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-principal-equipo**](a-msds-primarycomputer.md)                                     | False     | **Grupo**                                                                                                                          |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-TDO-salida-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-TDO-entrada-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nombre**](a-mssfu30name.md)                                                       | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-NIS-dominio**](a-mssfu30nisdomain.md)                                            | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                                        | False     | **Grupo**                                                                                                                          |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembro que no es de seguridad**](a-nonsecuritymember.md)                                           | False     | **Grupo**                                                                                                                          |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Miembros de grupo NT**](a-ntgroupmembers.md)                                                 | False     | **Grupo**                                                                                                                          |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                                     | True      | [**Arriba**](c-top.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto-categoría**](a-objectcategory.md)                                                  | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto**](a-objectclass.md)                                                        | True      | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Object-GUID**](a-objectguid.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Objeto: SID**](a-objectsid.md)                                                            | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Versión del objeto**](a-objectversion.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Operador-recuento**](a-operatorcount.md)                                                    | False     | **Grupo**                                                                                                                          |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Token de grupo principal**](a-primarygrouptoken.md)                                           | False     | **Grupo**                                                                                                                          |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Informes**](a-directreports.md)                                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes: desde**](a-repsfrom.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Representantes-a**](a-repsto.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Revisión**](a-revision.md)                                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Libra**](a-rid.md)                                                                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre de cuenta SAM**](a-samaccountname.md)                                                 | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo de cuenta SAM**](a-samaccounttype.md)                                                 | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificador de seguridad**](a-securityidentifier.md)                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Historial de SID**](a-sidhistory.md)                                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Referencias secundarias**](a-subrefs.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                                | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Marcas de sistema**](a-systemflags.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Número de teléfono**](a-telephonenumber.md)                                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Grupos de tokens**](a-tokengroups.md)                                                        | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-and-universal**](a-tokengroupsglobalanduniversal.md)                 | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-no-GC-aceptable**](a-tokengroupsnogcacceptable.md)                         | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario**](a-usercert.md)                                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**Contraseña de usuario**](a-userpassword.md)                                                      | False     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |
| [**USN: cambiado**](a-usnchanged.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: creado**](a-usncreated.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: entre sitios**](a-usnintersite.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**USN: origen**](a-usnsource.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuando se cambia**](a-whenchanged.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**Cuándo se crea**](a-whencreated.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**WWW-página-otro**](a-url.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Derechos extendidos de Windows Server 2012

Esta clase contiene los siguientes derechos extendidos para Windows Server 2012:



| Nombre común                  |
|------------------------------|
| [**Enviar a**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Escrituras validadas de Windows Server 2012

Esta clase contiene las siguientes escrituras validadas para Windows Server 2012:



| Nombre común                                  |
|----------------------------------------------|
| [**Suscripción automática**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Conjuntos de propiedades de Windows Server 2012

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2012:



| Nombre común                                      |
|--------------------------------------------------|
| [**Información de correo electrónico**](r-email-information.md) |



 

 





