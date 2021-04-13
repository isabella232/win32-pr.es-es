---
title: show sslcert
description: Enumera los enlaces de certificados de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- Mostrar sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358368"
---
# <a name="show-sslcert"></a><span data-ttu-id="b6dfc-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="b6dfc-104">show sslcert</span></span>

<span data-ttu-id="b6dfc-105">Enumera los enlaces de certificados de servidor SSL y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.</span><span class="sxs-lookup"><span data-stu-id="b6dfc-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="b6dfc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6dfc-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* dirección IP: Puerto*</span><span class="sxs-lookup"><span data-stu-id="b6dfc-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="b6dfc-108">Especifica la dirección IPv4 o IPv6 y el puerto para el que se mostrarán los enlaces de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="b6dfc-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="b6dfc-109">Si no se especifica un ipport, se enumeran todos los enlaces.</span><span class="sxs-lookup"><span data-stu-id="b6dfc-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b6dfc-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b6dfc-110">Examples</span></span>

<span data-ttu-id="b6dfc-111">**Show sslcert ipport = \[ fe80:: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="b6dfc-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="b6dfc-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="b6dfc-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="b6dfc-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="b6dfc-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="b6dfc-114">**Mostrar sslcert ipport = \[ ::: \] 443**</span><span class="sxs-lookup"><span data-stu-id="b6dfc-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




