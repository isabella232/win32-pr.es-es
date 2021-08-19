---
title: Clase Contact
description: Esta clase contiene información sobre una persona o empresa con la que puede que necesite ponerse en contacto periódicamente.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Esquema de AD de clase de contacto
- contact class AD Schema
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b54d5929e11382c1680090adf376f670d8610fd767a193e349a31f54c1f2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021893"
---
# <a name="contact-class"></a>Clase Contact

Esta clase contiene información sobre una persona o empresa con la que puede que necesite ponerse en contacto periódicamente.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Contacto                                        |
| Ldap-Display-Name | contact                                        |
| Actualizar privilegios  | El administrador del dominio establece este valor. |
| Frecuencia de actualización  | \-                                             |
| Schema-Id-Guid    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)
-   [Conjuntos de propiedades](#windows-2000-server-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000 Atributos de servidor

Esta clase contiene los atributos siguientes para Windows 2000 Server:



| Atributo                                                                 | Mandatory | Derivado de                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                 | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                               | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Employee-ID**](a-employeeid.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                        | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                   | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Último elemento primario conocido**](a-lastknownparent.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                               | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Consulte también**](a-seealso.md)                                             | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Sub refs**](a-subrefs.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                   | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                             | Falso     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                           | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                   | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                  | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Creado por USN**](a-usncreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objetos conocidos**](a-wellknownobjects.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                    | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Windows de propiedades del servidor 2000

Esta clase contiene los siguientes conjuntos de propiedades para Windows 2000 Server:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Personal-Information**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Conjuntos de propiedades](#windows-server-2003-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario del correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                   | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                   | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Employee-ID**](a-employeeid.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                          | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro nombre**](a-middlename.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte también**](a-seealso.md)                                               | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                         | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                               | Falso     | [**Person**](c-person.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                   | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                      | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Conjuntos de propiedades de Server 2003

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Conjuntos de propiedades](#windows-server-2003-r2-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario del correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                   | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                   | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                 | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Id. de empleado**](a-employeeid.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                     | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior Office box**](a-postofficebox.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte también**](a-seealso.md)                                               | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                         | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                               | Falso     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                   | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                     | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                      | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Conjuntos de propiedades de Server 2003 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003 R2:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Conjuntos de propiedades](#windows-server-2008-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario del correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                      | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                      | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                    | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Id. de empleado**](a-employeeid.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                             | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-LO-Seniority-Index**](a-msds-habseniorityindex.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                        | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro nombre**](a-middlename.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Postal-Address**](a-postaladdress.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte también**](a-seealso.md)                                                  | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                        | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                            | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sub refs**](a-subrefs.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                        | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                  | Falso     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                      | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                        | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Creado por USN**](a-usncreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                         | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Conjuntos de propiedades de Server 2008

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Personal-Information**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Conjuntos de propiedades](#windows-server-2008-r2-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los atributos siguientes para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                        | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                        | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                      | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Id. de empleado**](a-employeeid.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-LA-Seniority-Index**](a-msds-habseniorityindex.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro nombre**](a-middlename.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Postal-Address**](a-postaladdress.md)                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro Office posterior**](a-postofficebox.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                   | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte también**](a-seealso.md)                                                    | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                          | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                          | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                    | Falso     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                  | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                          | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Creado por USN**](a-usncreated.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objetos conocidos**](a-wellknownobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                           | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Conjuntos de propiedades de Server 2008 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008 R2:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Personal-Information**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Conjuntos de propiedades](#windows-server-2012-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor predeterminado de ocultación        | 0                                                                                            |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Unidad organizativa de DNS**](c-domaindns.md)[**de dominio**](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario del correo**](c-mailrecipient.md) (sistema)                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                              | Mandatory | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                                              | Falso     | **Contact**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Address-Home**](a-homepostaladdress.md)                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción del administrador**](a-admindescription.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Atributos permitidos**](a-allowedattributes.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Asistente**](a-assistant.md)                                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Canonical-Name**](a-canonicalname.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                                              | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                                            | Verdadero      | **Persona de** [ **contacto**](c-person.md)<br/> [**Destinatario del correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código de país**](a-countrycode.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de país**](a-c.md)                                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Firma DSA**](a-dsasignature.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Id. de empleado**](a-employeeid.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Banderas**](a-flags.md)                                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Desde entrada**](a-fromentry.md)                                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Período de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                                                     | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Given-Name**](a-givenname.md)                                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                                                | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se recicla**](a-isrecycled.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                                                     | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Locality-Name**](a-l.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                                        | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**director**](a-manager.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Mastered-By**](a-masteredby.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-GeoCoordinates-Altitude**](a-msds-geocoordinatesaltitude.md)                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                                 | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                               | Falso     | [**Destinatario del correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-LA-Seniority-Index**](a-msds-habseniorityindex.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | Falso     | **Contact**                                                                                                                            |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                                | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Category**](a-objectcategory.md)                                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Class**](a-objectclass.md)                                                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Guid de objeto**](a-objectguid.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-Version**](a-objectversion.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                                                       | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                                                | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Other-Name**](a-middlename.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Other**](a-otherhomephone.md)                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Home-Primary**](a-homephone.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Other**](a-otheripphone.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Ip-Primary**](a-ipphone.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Other**](a-othermobile.md)                                                            | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Mobile-Primary**](a-mobile.md)                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Office-Other**](a-othertelephone.md)                                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Other**](a-otherpager.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Pager-Primary**](a-pager.md)                                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles inferiores**](a-possibleinferiors.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                                              | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                                                    | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Preferred-Delivery-Method**](a-preferreddeliverymethod.md)                                         | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Rdn**](a-name.md)                                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Registered-Address**](a-registeredaddress.md)                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-From**](a-repsfrom.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Reps-To**](a-repsto.md)                                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                                       | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Consulte también**](a-seealso.md)                                                                          | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                                                | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                                                    | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**State-Or-Province-Name**](a-st.md)                                                                 | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sub refs**](a-subrefs.md)                                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Apellido**](a-sn.md)                                                                                | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas del sistema**](a-systemflags.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                                          | Falso     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de telex**](a-telexnumber.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Telex-Primary**](a-primarytelexnumber.md)                                                          | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Country**](a-co.md)                                                                           | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                                              | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Título**](a-title.md)                                                                               | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-Cert**](a-usercert.md)                                                                        | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**User-Comment**](a-comment.md)                                                                      | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                                                | Falso     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN cambiado**](a-usnchanged.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Creado por USN**](a-usncreated.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Intersite**](a-usnintersite.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Source**](a-usnsource.md)                                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Wbem-Path**](a-wbempath.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objetos conocidos**](a-wellknownobjects.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se crea**](a-whencreated.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page-Other**](a-url.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección X121**](a-x121address.md)                                                                  | Falso     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-Cert**](a-usercertificate.md)                                                                 | Falso     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Conjuntos de propiedades

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2012:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Personal-Information**](r-personal-information.md) |
| [**Información web**](r-web-information.md)           |



 

 





