---
description: El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tengan un patrón específico en un desplazamiento específico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Escribir el filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677666"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="d2056-103">Escribir el filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="d2056-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="d2056-104">El filtro de coincidencia de patrones notifica al controlador que acepte fotogramas que tengan un patrón específico en un desplazamiento específico.</span><span class="sxs-lookup"><span data-stu-id="d2056-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="d2056-105">Puede especificar un máximo de cuatro coincidencias de patrones detalladas, que se pueden combinar en instrucciones AND o or lógicas para Monitor de red evaluación de controladores.</span><span class="sxs-lookup"><span data-stu-id="d2056-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="d2056-106">Para implementar coincidencias de patrones, utilice las siguientes estructuras de Monitor de red:</span><span class="sxs-lookup"><span data-stu-id="d2056-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="d2056-107">**Expresiones**</span><span class="sxs-lookup"><span data-stu-id="d2056-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="d2056-108">**ANDEXP**</span><span class="sxs-lookup"><span data-stu-id="d2056-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="d2056-109">**PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="d2056-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="d2056-110">Para evaluar una instrucción **o** , combine dos a cuatro patrones que coincida con una estructura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="d2056-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="d2056-111">Para evaluar una instrucción y, combine una a cuatro estructuras **ANDEXP** y una estructura [**EXPRESSION**](expression.md) (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="d2056-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="d2056-112">Definiciones de coincidencia de patrones</span><span class="sxs-lookup"><span data-stu-id="d2056-112">Pattern Match Definitions</span></span>

<span data-ttu-id="d2056-113">La estructura [**PATTERNMATCH**](patternmatch.md) define una coincidencia de patrón única.</span><span class="sxs-lookup"><span data-stu-id="d2056-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="d2056-114">Una coincidencia individual puede funcionar de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="d2056-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="d2056-115">Normalmente, el controlador tomará la base de desplazamiento (que puede estar desplazada en relación con el \_ \_ \_ \_ marco, la base de desplazamiento \_ \_ \_ en relación con el \_ \_ Protocolo efectivo, la \_ base de desplazamiento \_ \_ en relación con \_ IPX o la \_ base de desplazamiento \_ con respecto \_ a la \_ dirección IP) e iniciar el recuento allí.</span><span class="sxs-lookup"><span data-stu-id="d2056-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="d2056-116">El controlador contará los bytes de desplazamiento desde allí y, después, coincidirá con los datos que encuentre con los bytes de primera longitud de **PatternToMatch**.</span><span class="sxs-lookup"><span data-stu-id="d2056-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="d2056-117">Si son iguales y \_ no se establecen las marcas de coincidencia de patrones \_ \_ no marcadas, se pasa este patrón.</span><span class="sxs-lookup"><span data-stu-id="d2056-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="d2056-118">Si son diferentes y \_ no se han establecido las marcas de coincidencia de patrones, se \_ \_ pasa el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2056-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="d2056-119">En caso contrario, se produce un error en este patrón.</span><span class="sxs-lookup"><span data-stu-id="d2056-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="d2056-120">O:</span><span class="sxs-lookup"><span data-stu-id="d2056-120">Or:</span></span>

<span data-ttu-id="d2056-121">Si \_ se establece la marca de marcas de coincidencia de patrones \_ \_ \_ especificada y la base se establece en desplazamiento de base con respecto a la base de \_ \_ \_ \_ IPX o de desplazamiento \_ \_ con respecto \_ a \_ la dirección IP, la comparación es más compleja.</span><span class="sxs-lookup"><span data-stu-id="d2056-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="d2056-122">En primer lugar, el controlador garantiza que el protocolo de base de desplazamiento está ahí, el controlador comprueba que el puerto especificado coincida con el puerto del marco.</span><span class="sxs-lookup"><span data-stu-id="d2056-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="d2056-123">Por último, el controlador garantiza que el miembro **PatternToMatch** coincide como antes, con la excepción de que el desplazamiento es del final de IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="d2056-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="d2056-124">Tenga en cuenta que si la base no es una de estas dos, se \_ omitirá el indicador de marcas de coincidencia de patrones \_ \_ \_ especificado y el patrón se evaluará como se ha indicado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d2056-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="d2056-125">Para evaluar una coincidencia de patrón única, una estructura de [**expresión**](expression.md) debe tener un miembro **AndExp** que contenga una coincidencia de patrón única.</span><span class="sxs-lookup"><span data-stu-id="d2056-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="d2056-126">La creación del filtro de coincidencia de patrones implica la creación de estructuras [**PATTERNMATCH**](patternmatch.md) y su combinación lógica con las estructuras [**Expression**](expression.md) y [**ANDEXP**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="d2056-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="d2056-127">**Para escribir un filtro de PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="d2056-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="d2056-128">En la estructura [**ANDEXP**](andexp.md) , rellene la matriz con coincidencias de patrones.</span><span class="sxs-lookup"><span data-stu-id="d2056-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="d2056-129">Rellene la estructura de [**expresión**](expression.md) con una matriz de miembros de **AndExp** .</span><span class="sxs-lookup"><span data-stu-id="d2056-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="d2056-130">No supere un total de cuatro coincidencias de patrón para el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d2056-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="d2056-131">En la estructura [**PATTERNMATCH**](patternmatch.md) , seleccione un tipo de marca.</span><span class="sxs-lookup"><span data-stu-id="d2056-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="d2056-132">Seleccione una base de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d2056-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="d2056-133">Enumerar un valor de puerto.</span><span class="sxs-lookup"><span data-stu-id="d2056-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="d2056-134">Defina el valor de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d2056-134">Define offset value.</span></span>
8.  <span data-ttu-id="d2056-135">Defina la longitud del patrón.</span><span class="sxs-lookup"><span data-stu-id="d2056-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="d2056-136">Enumera el valor del patrón.</span><span class="sxs-lookup"><span data-stu-id="d2056-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="d2056-137">Ejemplos de PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="d2056-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="d2056-138">Este marco representa un desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="d2056-138">This frame represents a standard offset.</span></span>

![marco de desplazamiento estándar](images/offs-pat.png)

<span data-ttu-id="d2056-140">El fragmento de código se implementa como:</span><span class="sxs-lookup"><span data-stu-id="d2056-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="d2056-141">Este marco representa un desplazamiento especificado por el puerto (contra IPX).</span><span class="sxs-lookup"><span data-stu-id="d2056-141">This frame depicts a port-specified offset (against IPX).</span></span>

![marco de desplazamiento especificado por el puerto](images/stan-pat.png)

<span data-ttu-id="d2056-143">El código de ejemplo se implementa como:</span><span class="sxs-lookup"><span data-stu-id="d2056-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



