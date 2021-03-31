---
title: atributo MS-FRS-Topology-Pref
description: El atributo MS-FRS-Topology-Pref se usa para registrar la configuración de topología de NTFRS preferida.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-FRS-Topology-Pref
- msFRS-Topology-atributo Pref AD Schema
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804651"
---
# <a name="ms-frs-topology-pref-attribute"></a>atributo MS-FRS-Topology-Pref

El atributo **MS-FRS-Topology-Pref** se usa para registrar la configuración de topología de NTFRS preferida. Cuando se agrega o se elimina un miembro de FRS en el conjunto de réplicas, se hace referencia a estos atributos y se realizan ajustes en las conexiones entre el resto de los miembros FRS del conjunto de réplicas.

Los valores válidos para este atributo son los siguientes.

| Value | Descripción                              |
|-------|------------------------------------------|
| 1     | \_anillo RSTOPOLOGYPREF de FRS \_<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | FRS \_ RSTOPOLOGYPREF \_ personalizado<br/>   |



 



| Entrada | Value |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Topology-Pref                                               |
| Nombre para mostrar de LDAP | msFRS-Topology-Pref                                                |
| Tamaño              | \-                                                                 |
| Actualizar privilegio  | Administrador de dominio                                               |
| Frecuencia de actualización  | Cuando se crea el conjunto de réplicas o se cambia la topología preferida. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID-GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Tiene un único valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Tiene un único valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Tiene un único valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Tiene un único valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Tiene un único valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> |



 

 





