---
title: Atributo ms-DNS-NSEC3-User-Salt
description: Atributo que define una cadena sal NSEC3 especificada por el usuario que se usará al firmar la zona DNS. Si está vacío, se usará sal aleatoria.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DNS-NSEC3-User-Salt
- msDNS-NSEC3UserSalt attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dbd1725675487ae5a6812dd77c400745b6671de0ef7db360e1c1980dd25b1b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553025"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>Atributo ms-DNS-NSEC3-User-Salt

Atributo que define una cadena sal NSEC3 especificada por el usuario que se usará al firmar la zona DNS. Si está vacío, se usará sal aleatoria.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DNS-NSEC3-User-Salt                      |
| Ldap-Display-Name | msDNS-NSEC3UserSalt                         |
| Size              | \-                                          |
| Actualizar privilegios  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-Id-Guid    | aff16770-9622-4fbc-a128-3088777605b9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------|
| Id. de vínculo                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Es de un solo valor       | Verdadero                                     |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**Dns-Zone**](c-dnszone.md)<br/> |



 

 





