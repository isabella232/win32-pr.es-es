---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Definición de ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "103797169"
---
# <a name="odj_policy_dns_domain_info-structure"></a>Estructura de ODJ_POLICY_DNS_DOMAIN_INFO

Contiene información sobre el dominio y el bosque a los que se debe unir un cliente.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>Miembros

### <a name="name"></a>NOMBRE

Debe establecerse en un nombre de dominio NetBIOS.

### <a name="dnsdomainname"></a>DnsDomainName

Debe establecerse en un nombre de dominio en formato DNS.

### <a name="dnsforestname"></a>Nombredebosquedns

Debe establecerse en un nombre de bosque en formato DNS.

### <a name="domainguid"></a>DomainGuid

Debe establecerse en el GUID del dominio.

### <a name="sid"></a>Sid

Debe establecerse en el SID del dominio.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**ODJ \_ cadena UNIcode \_**](odj-odj_unicode_string.md)

[**\_SID ODJ**](odj-odj_sid.md)
