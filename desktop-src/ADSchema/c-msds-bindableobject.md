---
title: clase de objeto MS-DS-Bindable
description: Clase auxiliar para representar un objeto enlazable. Cualquier clase definida por el usuario que representa una entidad que se puede utilizar para enlazar con el directorio (es decir, un usuario) debe incluir esta clase auxiliar.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- 'MS-DS-Bindable: esquema de AD de clase de objeto'
- Esquema de AD de la clase msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb69036ad9cd33b8f0a60f5356192acbea8dd71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905878"
---
# <a name="ms-ds-bindable-object-class"></a>clase de objeto MS-DS-Bindable

Clase auxiliar para representar un objeto enlazable. Cualquier clase definida por el usuario que representa una entidad que se puede utilizar para enlazar con el directorio (es decir, un usuario) debe incluir esta clase auxiliar.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Objeto MS-DS-Bindable                |
| Nombre para mostrar de LDAP | msDS-BindableObject                  |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Identificador de esquema-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementaciones

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Atributos](#adam-attributes)



| Entrada | Value |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | False                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Valor de ocultación predeterminada        | 1                                                            |
| RDN-ATT-ID                  | \-                                                           |
| Subclase de                 | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |
| Posibles superiores          | \-                                                           |
| Clases auxiliares           | \-                                                           |
| Descriptor de NT-Security-      | O:BAG: BAD: S:                                                 |
| Descriptor de seguridad predeterminado | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Atributos de ADAM

Esta clase contiene los siguientes atributos para ADAM:



| Atributo                                                                                      | Mandatory | Derivado de                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Cuenta-expira**](a-accountexpires.md)                                                    | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Admin: Descripción**](a-admindescription.md)                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos**](a-allowedattributes.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: atributos: efectivos**](a-allowedattributeseffective.md)                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido: clases secundarias**](a-allowedchildclasses.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Permitido-clases secundarias-eficaces**](a-allowedchildclasseseffective.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Hora de contraseña incorrecta**](a-badpasswordtime.md)                                                 | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Incorrecto: PWD-Count**](a-badpwdcount.md)                                                         | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Cabeza de puente-servidor-lista-BL**](a-bridgeheadserverlistbl.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre canónico**](a-canonicalname.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre común**](a-cn.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Creación: marca de tiempo**](a-createtimestamp.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Descripción**](a-description.md)                                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre para mostrar**](a-displayname.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**DS-Core-propagación-datos**](a-dscorepropagationdata.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**De entrada**](a-fromentry.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**FSMO: rol-Propietario**](a-fsmoroleowner.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Tipo de instancia**](a-instancetype.md)                                                        | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Se elimina**](a-isdeleted.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último conocido-primario**](a-lastknownparent.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Último inicio de sesión-marca de tiempo**](a-lastlogontimestamp.md)                                           | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Tiempo de bloqueo**](a-lockouttime.md)                                                          | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Objetos administrados**](a-managedobjects.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Maestro por**](a-masteredby.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Modificar: marca de tiempo**](a-modifytimestamp.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-aprox-immed-subordinados**](a-msds-approx-immed-subordinates.md)                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-MASTERD-by**](a-msds-masteredby.md)                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-cursores**](a-msds-ncreplcursors.md)                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-entrada-vecinos**](a-msds-ncreplinboundneighbors.md)                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-meta-data**](a-msds-replattributemetadata.md)                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Value-meta-data**](a-msds-replvaluemetadata.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**MS-DS-usuario-cuenta-bloqueo automático**](a-ms-ds-useraccountautolocked.md)                        | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)            | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-usuario-cuenta-deshabilitado**](a-msds-useraccountdisabled.md)                              | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-usuario-no-expire-contraseña**](a-msds-userdontexpirepassword.md)                       | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-usuario-cifrado-texto-contraseña-permitido**](a-ms-ds-userencryptedtextpasswordallowed.md) | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-User-Password-Expired**](a-msds-userpasswordexpired.md)                              | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**MS-DS-User-Password-Not-Required**](a-ms-ds-userpasswordnotrequired.md)                    | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**NT-pwd-History**](a-ntpwdhistory.md)                                                       | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Descriptor de NT-Security-**](a-ntsecuritydescriptor.md)                                       | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |
| [**Obj-Dist-nombre**](a-distinguishedname.md)                                                   | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto-categoría**](a-objectcategory.md)                                                    | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto**](a-objectclass.md)                                                          | True      | [**Arriba**](c-top.md)<br/>                                                              |
| [**Object-GUID**](a-objectguid.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Objeto: SID**](a-objectsid.md)                                                              | True      | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Versión del objeto**](a-objectversion.md)                                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Lista de atributos parciales eliminados**](a-partialattributedeletionlist.md)                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Conjunto de atributos parciales**](a-partialattributeset.md)                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Posibles: inferiores**](a-possibleinferiors.md)                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Nombre-objeto-proxy**](a-proxiedobjectname.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**PWD: último conjunto**](a-pwdlastset.md)                                                           | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**Query: Directiva-BL**](a-querypolicybl.md)                                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-data**](a-replpropertymetadata.md)                                      | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                           | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes: desde**](a-repsfrom.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Representantes-a**](a-repsto.md)                                                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Revisión**](a-revision.md)                                                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SD-derechos-efectivos**](a-sdrightseffective.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Servidor-referencia-BL**](a-serverreferencebl.md)                                             | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Mostrar en la vista avanzada**](a-showinadvancedviewonly.md)                                 | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Sitio-objeto-BL**](a-siteobjectbl.md)                                                       | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Clase de objeto estructural**](a-structuralobjectclass.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Referencias secundarias**](a-subrefs.md)                                                                  | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Adicionales: credenciales**](a-supplementalcredentials.md)                                  | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Marcas de sistema**](a-systemflags.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Grupos de tokens**](a-tokengroups.md)                                                          | False     | [**Entidad de seguridad**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-pwd**](a-unicodepwd.md)                                                            | False     | **Objeto MS-DS-Bindable**                                                                    |
| [**USN: cambiado**](a-usnchanged.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: creado**](a-usncreated.md)                                                            | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-quitado**](a-usndsalastobjremoved.md)                                     | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: entre sitios**](a-usnintersite.md)                                                        | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                    | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**USN: origen**](a-usnsource.md)                                                              | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WBEM: ruta de acceso**](a-wbempath.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                               | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuando se cambia**](a-whenchanged.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**Cuándo se crea**](a-whencreated.md)                                                          | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                         | False     | [**Arriba**](c-top.md)<br/>                                                              |
| [**WWW-página-otro**](a-url.md)                                                                | False     | [**Arriba**](c-top.md)<br/>                                                              |



 

 





