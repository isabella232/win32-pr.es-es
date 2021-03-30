---
title: atributo MS-DNS-NSEC3-usuario-Salt
description: Atributo que define una cadena de sal de NSEC3 especificada por el usuario que se va a usar al firmar la zona DNS. Si está vacío, se usará el valor Salt aleatorio.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DNS-NSEC3-usuario-sal
- msDN-NSEC3UserSalt atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804717"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>atributo MS-DNS-NSEC3-usuario-Salt

Atributo que define una cadena de sal de NSEC3 especificada por el usuario que se va a usar al firmar la zona DNS. Si está vacío, se usará el valor Salt aleatorio.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | MS-DNS-NSEC3-usuario-sal                      |
| Nombre para mostrar de LDAP | msDN: NSEC3UserSalt                         |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-ID-GUID    | aff16770-9622-4fbc-a128-3088777605b9        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | False                                    |
| Tiene un único valor       | True                                     |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**Zona DNS**](c-dnszone.md)<br/> |



 

 





