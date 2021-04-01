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
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="bad89-103">Estructura de ODJ_POLICY_DNS_DOMAIN_INFO</span><span class="sxs-lookup"><span data-stu-id="bad89-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="bad89-104">Contiene información sobre el dominio y el bosque a los que se debe unir un cliente.</span><span class="sxs-lookup"><span data-stu-id="bad89-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bad89-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bad89-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bad89-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="bad89-107">NOMBRE</span><span class="sxs-lookup"><span data-stu-id="bad89-107">Name</span></span>

<span data-ttu-id="bad89-108">Debe establecerse en un nombre de dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="bad89-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="bad89-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="bad89-109">DnsDomainName</span></span>

<span data-ttu-id="bad89-110">Debe establecerse en un nombre de dominio en formato DNS.</span><span class="sxs-lookup"><span data-stu-id="bad89-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="bad89-111">Nombredebosquedns</span><span class="sxs-lookup"><span data-stu-id="bad89-111">DnsForestName</span></span>

<span data-ttu-id="bad89-112">Debe establecerse en un nombre de bosque en formato DNS.</span><span class="sxs-lookup"><span data-stu-id="bad89-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="bad89-113">DomainGuid</span><span class="sxs-lookup"><span data-stu-id="bad89-113">DomainGuid</span></span>

<span data-ttu-id="bad89-114">Debe establecerse en el GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="bad89-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="bad89-115">Sid</span><span class="sxs-lookup"><span data-stu-id="bad89-115">Sid</span></span>

<span data-ttu-id="bad89-116">Debe establecerse en el SID del dominio.</span><span class="sxs-lookup"><span data-stu-id="bad89-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="bad89-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bad89-117">See also</span></span>

[<span data-ttu-id="bad89-118">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="bad89-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="bad89-119">**ODJ \_ cadena UNIcode \_**</span><span class="sxs-lookup"><span data-stu-id="bad89-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="bad89-120">**\_SID ODJ**</span><span class="sxs-lookup"><span data-stu-id="bad89-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
