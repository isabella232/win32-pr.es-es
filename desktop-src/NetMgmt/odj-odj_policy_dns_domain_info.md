---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO definición de IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566945"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO estructura

Contiene información sobre el dominio y el bosque al que se debe unir un cliente.

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

## <a name="members"></a>Members

### <a name="name"></a>NOMBRE

Debe establecerse en un nombre de dominio Netbios.

### <a name="dnsdomainname"></a>DnsDomainName

Debe establecerse en un nombre de dominio en formato DNS.

### <a name="dnsforestname"></a>DnsForestName

Debe establecerse en un nombre de bosque en formato DNS.

### <a name="domainguid"></a>DomainGuid

Debe establecerse en el GUID del dominio.

### <a name="sid"></a>Sid

Debe establecerse en el sid de dominio.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**CADENA \_ UNICODE ODJ \_**](odj-odj_unicode_string.md)

[**SID \_ de ODJ**](odj-odj_sid.md)
