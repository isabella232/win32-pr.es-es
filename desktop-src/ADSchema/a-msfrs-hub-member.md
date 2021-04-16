---
title: atributo MS-FRS-Hub-Member
description: El atributo MS-FRS-Hub-Member se usa para registrar la configuración de topología de NTFRS preferida.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-FRS-Hub-Member
- 'msFRS-Hub: esquema de AD de atributos de miembro'
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658846"
---
# <a name="ms-frs-hub-member-attribute"></a>atributo MS-FRS-Hub-Member

El atributo **MS-FRS-Hub-Member** se usa para registrar la configuración de topología de NTFRS preferida. Cuando se agrega o se elimina un miembro de FRS en un conjunto de réplicas, se hace referencia a estos atributos y se realizan los ajustes adecuados en las conexiones entre el resto de los miembros FRS del conjunto de réplicas.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------|
| CN                | Miembro de centro de MS-FRS                                                  |
| Nombre para mostrar de LDAP | msFRS: miembro central                                                   |
| Tamaño              | \-                                                                 |
| Actualizar privilegio  | Administrador de dominio                                               |
| Frecuencia de actualización  | Cuando se crea el conjunto de réplicas o se cambia la topología preferida. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID-GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Sintaxis            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------|
| Identificador de vínculo                | 1046                                                      |
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
| Identificador de vínculo                | 1046                                                      |
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
| Identificador de vínculo                | 1046                                                      |
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
| Identificador de vínculo                | 1046                                                      |
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
| Identificador de vínculo                | 1046                                                      |
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



## <a name="remarks"></a>Observaciones

Es el nombre distintivo completo de un objeto de [**NTFRS-Member**](c-ntfrsmember.md) . El nombre distintivo está en el formato de "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = volúmenes DFS, CN = servicio de replicación de archivos, CN = System, DC =..."

 

 





