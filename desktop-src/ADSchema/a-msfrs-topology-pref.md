---
title: Atributo ms-FRS-Topology-Pref
description: El atributo ms-FRS-Topology-Pref se usa para registrar la configuración de topología NTFRS preferida.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-FRS-Topology-Pref
- Esquema de AD del atributo msFRS-Topology-Pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8467a038db4f5c263253d31c33cb7dc01bb548712918d654b27b7778079d5c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960534"
---
# <a name="ms-frs-topology-pref-attribute"></a>Atributo ms-FRS-Topology-Pref

El **atributo ms-FRS-Topology-Pref** se usa para registrar la configuración de topología NTFRS preferida. Cuando se agrega o elimina un miembro FRS al conjunto de réplicas, se hace referencia a estos atributos y se realizan ajustes en las conexiones entre el resto de los miembros frs del conjunto de réplicas.

Los valores válidos para este atributo son los siguientes.

| Value | Descripción                              |
|-------|------------------------------------------|
| 1     | ANILLO \_ FRS RSTOPOLOGYPREF \_<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | FRS \_ RSTOPOLOGYPREF \_ PERSONALIZADO<br/>   |



 



| Entrada | Value |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Topology-Pref                                               |
| Ldap-Display-Name | msFRS-Topology-Pref                                                |
| Size              | \-                                                                 |
| Privilegio actualizar  | Administrador de dominio                                               |
| Frecuencia de actualización  | Cuando se crea el conjunto de réplicas o cambia la topología preferida. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-Id-Guid    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Es de un solo valor       | Verdadero                                                      |
| Está indexado             | Falso                                                     |
| En el catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Es de un solo valor       | Verdadero                                                      |
| Está indexado             | Falso                                                     |
| En el catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Es de un solo valor       | Verdadero                                                      |
| Está indexado             | Falso                                                     |
| En el catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Es de un solo valor       | Verdadero                                                      |
| Está indexado             | Falso                                                     |
| En el catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Es de un solo valor       | Verdadero                                                      |
| Está indexado             | Falso                                                     |
| En el catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



 

 





