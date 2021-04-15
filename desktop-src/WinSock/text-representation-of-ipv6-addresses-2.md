---
description: Esta sección se copia desde &\# 0034; arquitectura de direccionamiento IPv6&\# 0034; por R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representación de texto de direcciones IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715852"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="da8f3-103">Representación de texto de direcciones IPv6</span><span class="sxs-lookup"><span data-stu-id="da8f3-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="da8f3-104">R. Hinden y S. Deering copian esta sección de "arquitectura de direccionamiento IPv6".</span><span class="sxs-lookup"><span data-stu-id="da8f3-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="da8f3-105">Hay tres formas convencionales para representar direcciones IPv6 como cadenas de texto:</span><span class="sxs-lookup"><span data-stu-id="da8f3-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="da8f3-106">La forma preferida es x:x: x:x: x:x: x:x, donde ' x ' son los valores hexadecimales de las partes de 8 16 bits de la dirección.</span><span class="sxs-lookup"><span data-stu-id="da8f3-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="da8f3-107">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="da8f3-107">Examples:</span></span>

    <dl> <span data-ttu-id="da8f3-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="da8f3-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="da8f3-109">1080:0: 0:0: 8:800:200C: 417A</span><span class="sxs-lookup"><span data-stu-id="da8f3-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="da8f3-110">No es necesario escribir los ceros a la izquierda en un campo individual, pero debe haber al menos un número en cada campo (excepto en el caso descrito en el segundo formulario).</span><span class="sxs-lookup"><span data-stu-id="da8f3-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="da8f3-111">Debido al método de asignación de determinados estilos de direcciones IPv6, es habitual que las direcciones contengan cadenas largas de cero bits.</span><span class="sxs-lookup"><span data-stu-id="da8f3-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="da8f3-112">Con el fin de facilitar la escritura de direcciones que contienen cero bits, hay una sintaxis especial disponible para comprimir los ceros.</span><span class="sxs-lookup"><span data-stu-id="da8f3-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="da8f3-113">El uso de dos puntos dobles ("::") indica varios grupos de 16 bits de ceros.</span><span class="sxs-lookup"><span data-stu-id="da8f3-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="da8f3-114">Por ejemplo, la dirección de multidifusión</span><span class="sxs-lookup"><span data-stu-id="da8f3-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="da8f3-115">FF01:0: 0:0: 0:0: 0:43</span><span class="sxs-lookup"><span data-stu-id="da8f3-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="da8f3-116">se puede representar como:</span><span class="sxs-lookup"><span data-stu-id="da8f3-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="da8f3-117">FF01:: 43</span><span class="sxs-lookup"><span data-stu-id="da8f3-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="da8f3-118">Las comillas dobles ("::") solo pueden aparecer una vez en una dirección.</span><span class="sxs-lookup"><span data-stu-id="da8f3-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="da8f3-119">Se pueden usar para comprimir ceros iniciales o finales en una dirección.</span><span class="sxs-lookup"><span data-stu-id="da8f3-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="da8f3-120">Una forma alternativa que puede ser más conveniente cuando se trabaja con un entorno mixto de nodos IPv4 e IPv6 es x:x: x:x: x:x: d. d. d. d, donde ' x ' son los valores hexadecimales de los seis elementos de 16 bits de orden superior de la dirección, y los de la ' d ' son los valores decimales de las cuatro partes de 8 bits de orden inferior de la dirección (representación IPv4 estándar).</span><span class="sxs-lookup"><span data-stu-id="da8f3-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="da8f3-121">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="da8f3-121">Examples:</span></span>

    <dl> <span data-ttu-id="da8f3-122">0:0: 0:0: 0:0: 13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="da8f3-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="da8f3-123">0:0: 0:0: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="da8f3-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="da8f3-124">o en formato comprimido:</span><span class="sxs-lookup"><span data-stu-id="da8f3-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="da8f3-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="da8f3-125">::13.1.68.3</span></span>  
    <span data-ttu-id="da8f3-126">:: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="da8f3-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



