---
title: ms-DS-Resource-Property (clase)
description: Una instancia de esta clase contiene la definición de una propiedad en los recursos.
ms.assetid: 745048bc-d197-4ef1-a71c-46eb089a16d6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de la clase ms-DS-Resource-Property
- Esquema de AD de la clase msDS-ResourceProperty
topic_type:
- apiref
api_name:
- ms-DS-Resource-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11c390a0d9f4a9d54af58430d54ded84bf8b524c66c036fe93992891fd3034f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422546"
---
# <a name="ms-ds-resource-property-class"></a>ms-DS-Resource-Property (clase)

Una instancia de esta clase contiene la definición de una propiedad en los recursos.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Resource-Property              |
| Ldap-Display-Name | msDS-ResourceProperty                |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | 5b283d5e-8404-4195-9339-8450188c501a |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Valor |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                            |
| Object-Category             | 1                                                                                                |
| Default-Object-Category     | \-                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.273                                                                           |
| Valor predeterminado de ocultación        | 0                                                                                                |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Subclase de                 | [**ms-DS-Claim-Type-Property-Base**](c-msds-claimtypepropertybase.md)<br/>                |
| Posibles superiores          | [**ms-DS-Resource-Properties**](c-msds-resourceproperties.md)                                   |
| Clases auxiliares           | \-                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                     |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;; EA)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los atributos siguientes para Windows Server 2012:



| Atributo                                                                                        | Mandatory | Derivado de                                                                      |
|--------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Atributos permitidos**](a-allowedattributes.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Canonical-Name**](a-canonicalname.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Common-Name**](a-cn.md)                                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Descripción**](a-description.md)                                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Nombre para mostrar**](a-displayname.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Firma DSA**](a-dsasignature.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**habilitado**](a-enabled.md)                                                                     | Falso     | [**ms-DS-Claim-Type-Property-Base**](c-msds-claimtypepropertybase.md)<br/> |
| [**Nombre de extensión**](a-extensionname.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Banderas**](a-flags.md)                                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Desde entrada**](a-fromentry.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Tipo de instancia**](a-instancetype.md)                                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                                                   |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Se elimina**](a-isdeleted.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Is-Member-Of-DL**](a-memberof.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Se recicla**](a-isrecycled.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Objetos administrados**](a-managedobjects.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Mastered-By**](a-masteredby.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Applies-To-Resource-Types**](a-msds-appliestoresourcetypes.md)                         | Falso     | **ms-DS-Resource-Property**                                                       |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Claim-Possible-Values**](a-msds-claimpossiblevalues.md)                                | Falso     | [**ms-DS-Claim-Type-Property-Base**](c-msds-claimtypepropertybase.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With**](a-msds-claimsharespossiblevalueswith.md)          | Falso     | [**ms-DS-Claim-Type-Property-Base**](c-msds-claimtypepropertybase.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Is-Used-As-Resource-Security-Attribute**](a-msds-isusedasresourcesecurityattribute.md) | Falso     | **ms-DS-Resource-Property**                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-DS-Value-Type-Reference**](a-msds-valuetypereference.md)                                  | Verdadero      | **ms-DS-Resource-Property**                                                       |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                         | Verdadero      | [**Arriba**](c-top.md)<br/>                                                   |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Object-Category**](a-objectcategory.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                                                   |
| [**Object-Class**](a-objectclass.md)                                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                                                   |
| [**Guid de objeto**](a-objectguid.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Object-Version**](a-objectversion.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Posibles inferiores**](a-possibleinferiors.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Rdn**](a-name.md)                                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Informes**](a-directreports.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Reps-From**](a-repsfrom.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Reps-To**](a-repsto.md)                                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Revisión**](a-revision.md)                                                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Sub refs**](a-subrefs.md)                                                                    | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Marcas del sistema**](a-systemflags.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**USN cambiado**](a-usnchanged.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**UsN creado**](a-usncreated.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**USN-Intersite**](a-usnintersite.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**USN-Source**](a-usnsource.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Wbem-Path**](a-wbempath.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**Cuando se crea**](a-whencreated.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                                                   |
| [**WWW-Page-Other**](a-url.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                                                   |



 

 





