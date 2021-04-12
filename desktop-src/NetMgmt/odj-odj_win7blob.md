---
title: ODJ_WIN7BLOB
description: Definición de ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104359497"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="aa7a4-103">Estructura de ODJ_WIN7BLOB</span><span class="sxs-lookup"><span data-stu-id="aa7a4-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="aa7a4-104">Contiene la información básica necesaria para unir un cliente a un dominio.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa7a4-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="aa7a4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa7a4-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="aa7a4-107">lpDomain</span><span class="sxs-lookup"><span data-stu-id="aa7a4-107">lpDomain</span></span>

<span data-ttu-id="aa7a4-108">Debe establecerse en el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="aa7a4-109">lpMachineName</span><span class="sxs-lookup"><span data-stu-id="aa7a4-109">lpMachineName</span></span>

<span data-ttu-id="aa7a4-110">Debe establecerse en el nombre de la máquina.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="aa7a4-111">lpMachinePassword</span><span class="sxs-lookup"><span data-stu-id="aa7a4-111">lpMachinePassword</span></span>

<span data-ttu-id="aa7a4-112">Debe establecerse en una contraseña de texto no cifrado para la cuenta de equipo identificada por lpMachineName</span><span class="sxs-lookup"><span data-stu-id="aa7a4-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="aa7a4-113">DnsDomainInfo</span><span class="sxs-lookup"><span data-stu-id="aa7a4-113">DnsDomainInfo</span></span>

<span data-ttu-id="aa7a4-114">Contiene información sobre el dominio que se va a combinar.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="aa7a4-115">DcInfo</span><span class="sxs-lookup"><span data-stu-id="aa7a4-115">DcInfo</span></span>

<span data-ttu-id="aa7a4-116">Contiene información de nombre y dirección sobre el controlador de dominio que se usó para crear la cuenta de equipo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="aa7a4-117">Opciones</span><span class="sxs-lookup"><span data-stu-id="aa7a4-117">Options</span></span>

<span data-ttu-id="aa7a4-118">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa7a4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa7a4-119">See also</span></span>

[<span data-ttu-id="aa7a4-120">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="aa7a4-121">**\_información de \_ \_ dominio DNS de directiva \_ de ODJ**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="aa7a4-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



