---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO definición de IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d0a83ccade72a11449ca0cc9b35b9fc58e9c53d48f8248a9f6074cdb087cc0c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911605"
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

## <a name="members"></a>Miembros

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
