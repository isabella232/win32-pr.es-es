---
title: Establecimiento fuerte de tipos
description: C es un lenguaje débilmente tipado, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de tipos diferentes.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC llamada a procedimiento remoto, descripción, escritura de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994570"
---
# <a name="strong-typing"></a><span data-ttu-id="0bbe7-104">Establecimiento fuerte de tipos</span><span class="sxs-lookup"><span data-stu-id="0bbe7-104">Strong Typing</span></span>

<span data-ttu-id="0bbe7-105">C es un lenguaje débilmente tipado, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="0bbe7-106">Por ejemplo, C permite que el valor de una variable se convierta en otro tipo.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="0bbe7-107">La capacidad de usar variables de tipos diferentes en la misma expresión promueve la flexibilidad y la eficacia.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="0bbe7-108">Un lenguaje fuertemente tipado impone restricciones en las operaciones entre variables de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="0bbe7-109">En esos casos, el compilador emite un error que prohíbe la operación.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="0bbe7-110">Estas instrucciones estrictas relacionadas con los tipos de datos están diseñadas para evitar posibles errores.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="0bbe7-111">La dificultad de usar un lenguaje débilmente tipado, como C para llamadas a procedimientos remotos, es que las aplicaciones distribuidas se pueden ejecutar en varios equipos con compiladores de C diferentes y arquitecturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="0bbe7-112">Cuando una aplicación se ejecuta en un solo equipo, no tiene que preocuparse por el formato de datos interno, ya que los datos se administran de forma coherente.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="0bbe7-113">Sin embargo, en un entorno de computación distribuida, distintos equipos pueden usar definiciones diferentes para sus tipos de datos base.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="0bbe7-114">Por ejemplo, algunos equipos definen el tipo **int** , por lo que su representación interna es de 16 bits, mientras que otros usan 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="0bbe7-115">Una arquitectura de equipo, conocida como "little endian", asigna el byte menos significativo de los datos a la dirección de memoria más baja y el byte más significativo a la dirección más alta.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="0bbe7-116">Otra arquitectura, conocida como "big endian", asigna el byte menos significativo a la dirección de memoria más alta asociada a esos datos.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="0bbe7-117">Las llamadas a procedimientos remotos requieren un control estricto sobre los tipos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="0bbe7-118">Para controlar la transmisión y la conversión de datos a través de la red, MIDL exige estrictamente las restricciones de tipos para los datos transferidos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="0bbe7-119">Por esta razón, MIDL incluye un conjunto de [tipos base](base-types.md)bien definidos.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="0bbe7-120">MIDL exige el establecimiento fuerte de tipos, ya que exige el uso de palabras clave que definen sin ambigüedad el tamaño y el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="0bbe7-121">El efecto más visible de los tipos fuertes es que MIDL no permite variables del tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="0bbe7-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="0bbe7-122">En los temas siguientes, en esta sección se describen las características del lenguaje MIDL que aplican tipos de datos seguros:</span><span class="sxs-lookup"><span data-stu-id="0bbe7-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="0bbe7-123">Tipos base</span><span class="sxs-lookup"><span data-stu-id="0bbe7-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="0bbe7-124">Tipos con signo y sin signo</span><span class="sxs-lookup"><span data-stu-id="0bbe7-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="0bbe7-125">Tipos de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="0bbe7-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="0bbe7-126">Estructuras</span><span class="sxs-lookup"><span data-stu-id="0bbe7-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="0bbe7-127">Uniones</span><span class="sxs-lookup"><span data-stu-id="0bbe7-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="0bbe7-128">Tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="0bbe7-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="0bbe7-129">Matrices</span><span class="sxs-lookup"><span data-stu-id="0bbe7-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="0bbe7-130">Atributos de función</span><span class="sxs-lookup"><span data-stu-id="0bbe7-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="0bbe7-131">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="0bbe7-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="0bbe7-132">Tres tipos de puntero</span><span class="sxs-lookup"><span data-stu-id="0bbe7-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="0bbe7-133">Atributos de tipo</span><span class="sxs-lookup"><span data-stu-id="0bbe7-133">Type Attributes</span></span>](type-attributes.md)

 

 




