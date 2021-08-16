---
title: ms-DS-Bindable-Object (clase)
description: Clase auxiliar para representar un objeto enlazable. Cualquier clase definida por el usuario que represente una entidad que se pueda usar para enlazar con el directorio (es decir, un usuario), debe incluir esta clase auxiliar.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de la clase ms-DS-Bindable-Object
- Esquema de AD de la clase msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680785"
---
# <a name="ms-ds-bindable-object-class"></a>ms-DS-Bindable-Object (clase)

Clase auxiliar para representar un objeto enlazable. Cualquier clase definida por el usuario que represente una entidad que se pueda usar para enlazar con el directorio (es decir, un usuario), debe incluir esta clase auxiliar.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Bindable-Object                |
| Ldap-Display-Name | msDS-BindableObject                  |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementaciones

-   [**Adán**](#adam-attributes)

## <a name="adam"></a>Adán

-   [Atributos](#adam-attributes)



| Entrada | Valor |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Falso                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Valor predeterminado de ocultación        | 1                                                            |
| Rdn-Att-Id                  | \-                                                           |
| Subclase de                 | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| Posibles superiores          | \-                                                           |
| Clases auxiliares           | \-                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                 |
| Descriptor de seguridad predeterminado | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Atributos ADAM

Esta clase contiene los atributos siguientes para ADAM:



| Atributo                                                                                      | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Expires**](a-accountexpires.md)                                                    | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Descripción del administrador**](a-admindescription.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Atributos permitidos**](a-allowedattributes.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tiempo de contraseña incorrecta**](a-badpasswordtime.md)                                                 | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Bad-Pwd-Count**](a-badpwdcount.md)                                                         | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre común**](a-cn.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Crear marca de tiempo**](a-createtimestamp.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre para mostrar**](a-displayname.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Desde entrada**](a-fromentry.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tipo de instancia**](a-instancetype.md)                                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Member-Of-DL**](a-memberof.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Marca de tiempo del último inicio de sesión**](a-lastlogontimestamp.md)                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Tiempo de bloqueo**](a-lockouttime.md)                                                          | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-Auto-Locked**](a-ms-ds-useraccountautolocked.md)                        | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Disabled**](a-msds-useraccountdisabled.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Dont-Expire-Password**](a-msds-userdontexpirepassword.md)                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-Allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Expired**](a-msds-userpasswordexpired.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Not-Required**](a-ms-ds-userpasswordnotrequired.md)                    | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Nt-Pwd-History**](a-ntpwdhistory.md)                                                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                       | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Category**](a-objectcategory.md)                                                    | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Class**](a-objectclass.md)                                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Guid de objeto**](a-objectguid.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                                              | Verdadero      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Object-Version**](a-objectversion.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles inferiores**](a-possibleinferiors.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Pwd-Last-Set**](a-pwdlastset.md)                                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sub refs**](a-subrefs.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Credenciales complementarias**](a-supplementalcredentials.md)                                  | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas del sistema**](a-systemflags.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                                          | Falso     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-Pwd**](a-unicodepwd.md)                                                            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**USN cambiado**](a-usnchanged.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Creado por USN**](a-usncreated.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objetos conocidos**](a-wellknownobjects.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se crea**](a-whencreated.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                              |



 

 





