---
title: clase ms-DS-Service-Connection-Point-Publication-Service
description: Almacena las opciones de configuración para el servicio de publicación de punto de conexión de servicio en ADAM.
ms.assetid: 30b4df70-a03b-4d42-b200-75bfa6cf8273
ms.tgt_platform: multiple
keywords:
- Esquema de AD de la clase ms-DS-Service-Connection-Point-Publication-Service
- Esquema de AD de la clase msDS-ServiceConnectionPointPublicationService
topic_type:
- apiref
api_name:
- ms-DS-Service-Connection-Point-Publication-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b458a5d66d8d6fd90a58519ce57de03f625087be4123f2e51ca8c09534ed96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879845"
---
# <a name="ms-ds-service-connection-point-publication-service-class"></a>clase ms-DS-Service-Connection-Point-Publication-Service

Almacena las opciones de configuración para el servicio de publicación de punto de conexión de servicio en ADAM.



| Entrada | Value |
|-------------------|----------------------------------------------------|
| CN                | ms-DS-Service-Connection-Point-Publication-Service |
| Ldap-Display-Name | msDS-ServiceConnectionPointPublicationService      |
| Privilegio actualizar  | \-                                                 |
| Frecuencia de actualización  | \-                                                 |
| Schema-Id-Guid    | d33f5da6-b009-7e48-8268-b2305529e933               |



## <a name="implementations"></a>Implementaciones

-   [**Adán**](#adam-attributes)

## <a name="adam"></a>Adán

-   [Atributos](#adam-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------|
| System-Only                 | Verdadero                                   |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.5.247                 |
| Valor predeterminado de ocultación        | 1                                      |
| Rdn-Att-Id                  | [**Nombre común**](a-cn.md)<br/> |
| Subclase de                 | [**Arriba**](c-top.md)<br/>        |
| Posibles superiores          | [**NTDS-Service**](c-ntdsservice.md)  |
| Clases auxiliares           | \-                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                           |
| Descriptor de seguridad predeterminado | D:S:                                   |
| System-Flags                | 0x00000000                             |



## <a name="adam-attributes"></a>Atributos ADAM

Esta clase contiene los atributos siguientes para ADAM:



| Atributo                                                                   | Mandatory | Derivado de                                           |
|-----------------------------------------------------------------------------|-----------|--------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Nombre común**](a-cn.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Crear marca de tiempo**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**habilitado**](a-enabled.md)                                                | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                        |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Palabras clave**](a-keywords.md)                                              | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-Disable-For-Instances**](a-msds-disableforinstances.md)           | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**ms-DS-SCP-Container**](a-msds-scpcontainer.md)                          | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                        |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                        |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Well-Known-Objects**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                        |



 

 





