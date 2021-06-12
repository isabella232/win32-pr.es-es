---
title: Registros de recursos
description: Obtenga información sobre los registros de recursos. Un registro de recursos es la unidad de entrada de información en los archivos de zona DNS, que se usa para resolver todas las consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010678"
---
# <a name="resource-records"></a><span data-ttu-id="8184e-104">Registros de recursos</span><span class="sxs-lookup"><span data-stu-id="8184e-104">Resource Records</span></span>

<span data-ttu-id="8184e-105">Un registro de recursos, conocido normalmente como RR, es la unidad de entrada de información en los archivos de zona DNS. Los RR son los bloques de creación básicos de la información ip y el nombre de host y se usan para resolver todas las consultas DNS.</span><span class="sxs-lookup"><span data-stu-id="8184e-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="8184e-106">Los registros de recursos existen tantos tipos para proporcionar servicios extendidos de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="8184e-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="8184e-107">Los distintos tipos de RR tienen formatos diferentes, ya que contienen datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8184e-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="8184e-108">Sin embargo, en general, muchos RR comparten un formato común, como se muestra en el ejemplo de registros de recursos de dirección siguientes.</span><span class="sxs-lookup"><span data-stu-id="8184e-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="8184e-109">En el ejemplo ficticio siguiente se explican los campos que se encuentran en un registro de recursos A:</span><span class="sxs-lookup"><span data-stu-id="8184e-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="8184e-110">El primer campo (microsoft.com) indica el propietario.</span><span class="sxs-lookup"><span data-stu-id="8184e-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="8184e-111">El segundo campo (600) es el parámetro de período de vida (TTL), en segundos.</span><span class="sxs-lookup"><span data-stu-id="8184e-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="8184e-112">El tercer campo (IN) es el campo de clase que representa la familia de protocolos, que casi siempre es IN, para la clase de Internet.</span><span class="sxs-lookup"><span data-stu-id="8184e-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="8184e-113">El cuarto campo (A) es el tipo de recurso que el RR representa.</span><span class="sxs-lookup"><span data-stu-id="8184e-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="8184e-114">El quinto campo (150.150.150.1) son los datos de recursos o RDATA.</span><span class="sxs-lookup"><span data-stu-id="8184e-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="8184e-115">Este campo es un tipo de variable que proporciona información adecuada para el tipo de recurso; En este caso, es una dirección IP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8184e-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="8184e-116">Los siguientes tipos de registro de recursos se usan normalmente en DNS:</span><span class="sxs-lookup"><span data-stu-id="8184e-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="8184e-117">Inicio de autoridad (SOA)</span><span class="sxs-lookup"><span data-stu-id="8184e-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="8184e-118">Servidor de nombres (NS)</span><span class="sxs-lookup"><span data-stu-id="8184e-118">Name server (NS)</span></span>
-   <span data-ttu-id="8184e-119">[*Registro de puntero*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="8184e-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="8184e-120">Dirección (A)</span><span class="sxs-lookup"><span data-stu-id="8184e-120">Address (A)</span></span>
-   <span data-ttu-id="8184e-121">Dirección IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="8184e-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="8184e-122">Intercambio de correo (MX)</span><span class="sxs-lookup"><span data-stu-id="8184e-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="8184e-123">[*Nombre canónico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="8184e-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="8184e-124">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="8184e-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="8184e-125">Búsqueda inversa de WINS (WINSR)</span><span class="sxs-lookup"><span data-stu-id="8184e-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="8184e-126">Hay muchos otros tipos de registros de recursos en DNS.</span><span class="sxs-lookup"><span data-stu-id="8184e-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="8184e-127">Para obtener más información, vea [Referencia del proveedor WMI de DNS.](dns-wmi-provider-reference.md)</span><span class="sxs-lookup"><span data-stu-id="8184e-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




