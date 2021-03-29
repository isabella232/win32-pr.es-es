---
title: Registros de recursos
description: Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778336"
---
# <a name="resource-records"></a><span data-ttu-id="047d7-103">Registros de recursos</span><span class="sxs-lookup"><span data-stu-id="047d7-103">Resource Records</span></span>

<span data-ttu-id="047d7-104">Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS.</span><span class="sxs-lookup"><span data-stu-id="047d7-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="047d7-105">Los registros de recursos existen tantos tipos para proporcionar servicios extendidos de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="047d7-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="047d7-106">Los distintos tipos de RRs tienen formatos diferentes, ya que contienen datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="047d7-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="047d7-107">Sin embargo, en general, muchos RRs comparten un formato común, como se muestra en el siguiente ejemplo de registros de recursos de dirección.</span><span class="sxs-lookup"><span data-stu-id="047d7-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="047d7-108">En el siguiente ejemplo ficticio se explican los campos que se encuentran en un registro de recursos A:</span><span class="sxs-lookup"><span data-stu-id="047d7-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="047d7-109">El primer campo (microsoft.com) denota el propietario.</span><span class="sxs-lookup"><span data-stu-id="047d7-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="047d7-110">El segundo campo (600) es el parámetro de período de vida (TTL), en segundos.</span><span class="sxs-lookup"><span data-stu-id="047d7-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="047d7-111">El tercer campo (en) es el campo de clase que representa la familia de protocolos, que casi siempre está en, para la clase de Internet.</span><span class="sxs-lookup"><span data-stu-id="047d7-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="047d7-112">El cuarto campo (A) es el tipo de recurso que representa el RR.</span><span class="sxs-lookup"><span data-stu-id="047d7-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="047d7-113">El quinto campo (150.150.150.1) son los datos de recursos o RDATA.</span><span class="sxs-lookup"><span data-stu-id="047d7-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="047d7-114">Este campo es un tipo de variable que proporciona información adecuada para el tipo de recurso. en este caso, se trata de una dirección IP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="047d7-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="047d7-115">Los siguientes tipos de registro de recursos se usan normalmente en DNS:</span><span class="sxs-lookup"><span data-stu-id="047d7-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="047d7-116">Inicio de autoridad (SOA)</span><span class="sxs-lookup"><span data-stu-id="047d7-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="047d7-117">Servidor de nombres (NS)</span><span class="sxs-lookup"><span data-stu-id="047d7-117">Name server (NS)</span></span>
-   <span data-ttu-id="047d7-118">[*Registro de puntero*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="047d7-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="047d7-119">Dirección (A)</span><span class="sxs-lookup"><span data-stu-id="047d7-119">Address (A)</span></span>
-   <span data-ttu-id="047d7-120">Dirección IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="047d7-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="047d7-121">Intercambio de correo (MX)</span><span class="sxs-lookup"><span data-stu-id="047d7-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="047d7-122">[*Nombre canónico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="047d7-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="047d7-123">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="047d7-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="047d7-124">Búsqueda inversa de WINS (WINSr)</span><span class="sxs-lookup"><span data-stu-id="047d7-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="047d7-125">Hay muchos otros tipos de registros de recursos en DNS.</span><span class="sxs-lookup"><span data-stu-id="047d7-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="047d7-126">Para obtener más información, vea [Referencia del proveedor WMI de DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="047d7-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




