---
title: Clase Contact
description: Esta clase contiene información sobre una persona o compañía que puede necesitar para ponerse en contacto con regularidad.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Esquema de la clase Contact AD
- Esquema de la clase Contact AD
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab728fbd87007f01076405730dcfee9f6d935a23
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493643"
---
# <a name="contact-class"></a>Clase Contact

Esta clase contiene información sobre una persona o compañía que puede necesitar para ponerse en contacto con regularidad.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Contacto                                        |
| Nombre para mostrar de LDAP | contact                                        |
| Actualizar privilegio  | El administrador del dominio establece este valor. |
| Frecuencia de actualización  | \-                                             |
| Identificador de esquema-GUID    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



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
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Atributos de servidor de Windows 2000

Esta clase contiene los siguientes atributos para el servidor de Windows 2000:



| Atributo                                                                 | Mandatory | Derivado de                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                 | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                               | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                   | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Último conocido-primario**](a-lastknownparent.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                  | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                               | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                     | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Vea también**](a-seealso.md)                                             | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Referencias secundarias**](a-subrefs.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                   | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                             | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                   | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                  | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Conjuntos de propiedades de servidor de Windows 2000

Esta clase contiene los siguientes conjuntos de propiedades para el servidor de Windows 2000:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)
-   [Conjuntos de propiedades](#windows-server-2003-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Atributos de Windows Server 2003

Esta clase contiene los siguientes atributos para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                   | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                   | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                 | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-permitido a delegado a**](a-msds-allowedtodelegateto.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Vea también**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                   | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Conjuntos de propiedades de Windows Server 2003

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)
-   [Conjuntos de propiedades](#windows-server-2003-r2-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Atributos de Windows Server 2003 R2

Esta clase contiene los siguientes atributos para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                   | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                   | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                 | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                     | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último conocido-primario**](a-lastknownparent.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-permitido a delegado a**](a-msds-allowedtodelegateto.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | False     | **Contacto**                                                                                                                            |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                    | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                                 | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                       | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Vea también**](a-seealso.md)                                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Referencias secundarias**](a-subrefs.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                               | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                   | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                     | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Conjuntos de propiedades de Windows Server 2003 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2003 R2:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)
-   [Conjuntos de propiedades](#windows-server-2008-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Atributos de Windows Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                      | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                    | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                        | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                             | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último conocido-primario**](a-lastknownparent.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-permitido a delegado a**](a-msds-allowedtodelegateto.md)             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de la compañía MS-DS-Phonetic**](a-msds-phoneticcompanyname.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Departamento**](a-msds-phoneticdepartment.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                |
| [**MS-DS-fonética-First-Name**](a-msds-phoneticfirstname.md)                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | False     | **Contacto**                                                                                                                            |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                       | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                                    | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                          | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Vea también**](a-seealso.md)                                                  | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                            | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Referencias secundarias**](a-subrefs.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                  | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                      | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                        | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Conjuntos de propiedades de Windows Server 2008

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)
-   [Conjuntos de propiedades](#windows-server-2008-r2-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Atributos de Windows Server 2008 R2

Esta clase contiene los siguientes atributos para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                        | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                      | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                          | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se recicla**](a-isrecycled.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último conocido-primario**](a-lastknownparent.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-permitido a delegado a**](a-msds-allowedtodelegateto.md)               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md) | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de la compañía MS-DS-Phonetic**](a-msds-phoneticcompanyname.md)                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Departamento**](a-msds-phoneticdepartment.md)                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                |
| [**MS-DS-fonética-First-Name**](a-msds-phoneticfirstname.md)                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | False     | **Contacto**                                                                                                                            |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                          | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                         | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                                      | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                            | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)                   | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Vea también**](a-seealso.md)                                                    | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Referencias secundarias**](a-subrefs.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                    | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                                  | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                         | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                           | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Conjuntos de propiedades de Windows Server 2008 R2

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2008 R2:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)
-   [Conjuntos de propiedades](#windows-server-2012-property-sets)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | [**Person**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valor de ocultación predeterminada        | 0                                                                                            |
| RDN-ATT-ID                  | [**Nombre común**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Posibles superiores          | [**Dominio-**](c-domaindns.md)[**unidad organizativa de** DNS](c-organizationalunit.md)         |
| Clases auxiliares           | [**Destinatario de correo**](c-mailrecipient.md) (sistema)                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                                                 |
| Descriptor de seguridad predeterminado | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; ESTÉ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Atributos de Windows Server 2012

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                              | Mandatory | Derivado de                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Información adicional**](a-notes.md)                                                              | False     | **Contacto**                                                                                                                            |
| [**Dirección**](a-streetaddress.md)                                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección: Inicio**](a-homepostaladdress.md)                                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Admin: Descripción**](a-admindescription.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos**](a-allowedattributes.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Para**](a-assistant.md)                                                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre canónico**](a-canonicalname.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Comentario**](a-info.md)                                                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nombre común**](a-cn.md)                                                                            | True      |  [ **Persona** de contacto](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Compañía**](a-company.md)                                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**País: código**](a-countrycode.md)                                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre del país**](a-c.md)                                                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Departamento**](a-department.md)                                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Descripción**](a-description.md)                                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Indicador de destino**](a-destinationindicator.md)                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre para mostrar**](a-displayname.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Display-Name-printable**](a-displaynameprintable.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**División**](a-division.md)                                                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-firma**](a-dsasignature.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones de correo electrónico**](a-mail.md)                                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**IDENTIFICADOR de empleado**](a-employeeid.md)                                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de extensión**](a-extensionname.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Fax-número de teléfono**](a-facsimiletelephonenumber.md)                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Marcas**](a-flags.md)                                                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**De entrada**](a-fromentry.md)                                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tiempo de intercalación de elementos no utilizados**](a-garbagecollperiod.md)                                                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Calificador de generación**](a-generationqualifier.md)                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre dado**](a-givenname.md)                                                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Iniciales**](a-initials.md)                                                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tipo de instancia**](a-instancetype.md)                                                                | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**International-ISDN (número)**](a-internationalisdnnumber.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se elimina**](a-isdeleted.md)                                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Is-member-of-DL**](a-memberof.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Es-titular de privilegios**](a-isprivilegeholder.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Se recicla**](a-isrecycled.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                                                     | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Último conocido-primario**](a-lastknownparent.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Heredado-Exchange-DN**](a-legacyexchangedn.md)                                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localidad: nombre**](a-l.md)                                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logotipo**](a-thumbnaillogo.md)                                                                        | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objetos administrados**](a-managedobjects.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Maestro por**](a-masteredby.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-allowed-to-Act-on-nombre-of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-permitido a delegado a**](a-msds-allowedtodelegateto.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Claim-shares-posibles-Values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-geocoordinations-altitud**](a-msds-geocoordinatesaltitude.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-geocoordinations-latitud**](a-msds-geocoordinateslatitude.md)                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-geocoordinations-longitud**](a-msds-geocoordinateslongitude.md)                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-domain-para**](a-msds-isdomainfor.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-FULL-Replica-para**](a-msds-isfullreplicafor.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-Partial-Replica-para**](a-msds-ispartialreplicafor.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-IS-Primary-Computer-para**](a-msds-isprimarycomputerfor.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-known-RDN**](a-msds-lastknownrdn.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-local-de eliminación efectiva**](a-msds-localeffectivedeletiontime.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-local-vigencia-reciclaje-hora**](a-msds-localeffectiverecycletime.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-role-BL**](a-msds-membersforazrolebl.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Tipo MS-DS-NC**](a-msds-nctype.md)                                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-non-Members-BL**](a-msds-nonmembersbl.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-role-BL**](a-msds-operationsforazrolebl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de la compañía MS-DS-Phonetic**](a-msds-phoneticcompanyname.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Departamento**](a-msds-phoneticdepartment.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de MS-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                |
| [**MS-DS-fonética-First-Name**](a-msds-phoneticfirstname.md)                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la entidad de seguridad de MS-DS**](a-msds-principalname.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO: aplicado**](a-msds-psoapplied.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelód-DSA**](a-msds-revealeddsas.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Revelad-List-BL**](a-msds-revealedlistbl.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | False     | **Contacto**                                                                                                                            |
| [**MS-DS-Tasks-for-AZ-role-BL**](a-msds-tasksforazrolebl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-TDO-salida-BL**](a-msds-tdoegressbl.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-TDO-entrada-BL**](a-msds-tdoingressbl.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre MS-Exch-Assistant**](a-msexchassistantname.md)                                                | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-Exch-Owner-BL**](a-ownerbl.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                                               | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                                           | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Objeto-categoría**](a-objectcategory.md)                                                            | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Clase de objeto**](a-objectclass.md)                                                                  | True      | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Object-GUID**](a-objectguid.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Versión del objeto**](a-objectversion.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de unidad organizativa**](a-ou.md)                                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre de la organización**](a-o.md)                                                                       | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro buzón de correo**](a-othermailbox.md)                                                                | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otro: nombre**](a-middlename.md)                                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Título personal**](a-personaltitle.md)                                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-fax-otro**](a-otherfacsimiletelephonenumber.md)                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-otro**](a-otherhomephone.md)                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-Inicio-principal**](a-homephone.md)                                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-otro**](a-otheripphone.md)                                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-IP-principal**](a-ipphone.md)                                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-ISDN-principal**](a-primaryinternationalisdnnumber.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono móvil-otro**](a-othermobile.md)                                                            | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-móvil-principal**](a-mobile.md)                                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono-oficina-otros**](a-othertelephone.md)                                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas-otro**](a-otherpager.md)                                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Teléfono: buscapersonas: principal**](a-pager.md)                                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Imagen**](a-thumbnailphoto.md)                                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección postal**](a-postaladdress.md)                                                              | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Código postal**](a-postalcode.md)                                                                    | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Cuadro posterior a la oficina**](a-postofficebox.md)                                                             | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Método de entrega preferido**](a-preferreddeliverymethod.md)                                         | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Dirección registrada**](a-registeredaddress.md)                                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Informes**](a-directreports.md)                                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes: desde**](a-repsfrom.md)                                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Representantes-a**](a-repsto.md)                                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Revisión**](a-revision.md)                                                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                                       | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Vea también**](a-seealso.md)                                                                          | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Número de serie**](a-serialnumber.md)                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Mostrar en la libreta de direcciones**](a-showinaddressbook.md)                                                    | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                                               | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Nombre de estado o provincia**](a-st.md)                                                                 | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Dirección postal**](a-street.md)                                                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Referencias secundarias**](a-subrefs.md)                                                                          | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**2º**](a-sn.md)                                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Marcas de sistema**](a-systemflags.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Número de teléfono**](a-telephonenumber.md)                                                          | False     | [**Person**](c-person.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/>                                             |
| [**Teletexto: identificador de terminal**](a-teletexterminalidentifier.md)                                     | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Número de télex**](a-telexnumber.md)                                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex: principal**](a-primarytelexnumber.md)                                                          | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texto: país**](a-co.md)                                                                           | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Codificación de texto o dirección**](a-textencodedoraddress.md)                                              | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Title**](a-title.md)                                                                               | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Certificado de usuario**](a-usercert.md)                                                                        | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**Comentario de usuario**](a-comment.md)                                                                      | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Contraseña de usuario**](a-userpassword.md)                                                                | False     | [**Person**](c-person.md)<br/>                                                                                                  |
| [**Certificado de usuario SMIME**](a-usersmimecertificate.md)                                               | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN: cambiado**](a-usnchanged.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: creado**](a-usncreated.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: entre sitios**](a-usnintersite.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**USN: origen**](a-usnsource.md)                                                                      | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuando se cambia**](a-whenchanged.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**Cuándo se crea**](a-whencreated.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                                 | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**WWW-página-otro**](a-url.md)                                                                        | False     | [**Arriba**](c-top.md)<br/>                                                                                                        |
| [**X121-Address**](a-x121address.md)                                                                  | False     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                                                 | False     | [**Destinatario de correo**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Conjuntos de propiedades de Windows Server 2012

Esta clase contiene los siguientes conjuntos de propiedades para Windows Server 2012:



| Nombre común                                            |
|--------------------------------------------------------|
| [**Información personal**](r-personal-information.md) |
| [**Información Web**](r-web-information.md)           |



 

 





