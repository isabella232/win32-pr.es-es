---
title: Atributo ms-FRS-Hub-Member
description: El atributo ms-FRS-Hub-Member se usa para registrar la configuración de topología NTFRS preferida.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-FRS-Hub-Member
- Esquema de AD del atributo msFRS-Hub-Member
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f2cc1014b081ac13183144fca34c2087539de0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885707"
---
# <a name="ms-frs-hub-member-attribute"></a>Atributo ms-FRS-Hub-Member

El **atributo ms-FRS-Hub-Member** se usa para registrar la configuración de topología NTFRS preferida. Cuando se agrega o elimina un miembro de FRS a un conjunto de réplicas, se hace referencia a estos atributos y se realizan los ajustes adecuados en las conexiones entre el resto de los miembros frs del conjunto de réplicas.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Hub-Member                                                  |
| Ldap-Display-Name | msFRS-Hub-Member                                                   |
| Size              | \-                                                                 |
| Actualizar privilegios  | Administrador de dominio                                               |
| Frecuencia de actualización  | Cuando se crea el conjunto de réplicas o cambia la topología preferida. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-Id-Guid    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Es de un solo valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Es de un solo valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Es de un solo valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Es de un solo valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| Id. de vínculo                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Es de un solo valor       | True                                                      |
| Está indexado             | False                                                     |
| En el catálogo global      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Clases usadas en        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Comentarios

Este es el nombre distintivo completo de un [**objeto NTFRS-Member.**](c-ntfrsmember.md) El nombre distintivo tiene el formato "CN=*&lt; &gt; computerGuid*, CN= *<Dfs Link Name>* , CN= , *<Dfs Root name>* CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."

 

 





