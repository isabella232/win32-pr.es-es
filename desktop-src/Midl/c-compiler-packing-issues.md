---
title: Problemas de empaquetado del compilador de C
description: Los niveles de empaquetado afectan al diseño de memoria de los tipos de MIDL y del compilador de C/C++ de Microsoft de la misma manera.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- 'MIDL del compilador MIDL; C: problemas de empaquetado del compilador'
- empaquetar MIDL
- MIDL de diseño de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904570"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="96697-106">Problemas de empaquetado del compilador de C</span><span class="sxs-lookup"><span data-stu-id="96697-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="96697-107">Los niveles de empaquetado afectan al diseño de memoria de los tipos de MIDL y del compilador de C/C++ de Microsoft de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="96697-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="96697-108">En entornos de compilación de Microsoft, como el entorno de compilación definido por VC + + o el kit de desarrollo de software (SDK) de plataforma, el nivel de empaquetado predeterminado para los compiladores de MIDL y C/C++ es el mismo. el nivel de empaquetado predeterminado para los entornos de compilación de Windows de 32 y 64 bits es 8.</span><span class="sxs-lookup"><span data-stu-id="96697-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="96697-109">Alineación natural</span><span class="sxs-lookup"><span data-stu-id="96697-109">Natural Alignment</span></span>

<span data-ttu-id="96697-110">En el caso de los tipos de memoria, la alineación predeterminada es la misma que su alineación natural.</span><span class="sxs-lookup"><span data-stu-id="96697-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="96697-111">Un tipo base, como Short, Float e \_ \_ Int64, y un puntero se alinea de forma natural si su representación comienza en una dirección cuyo tamaño es módulo.</span><span class="sxs-lookup"><span data-stu-id="96697-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="96697-112">Todos los tipos base admitidos actualmente tienen tamaños de 1, 2, 4 u 8.</span><span class="sxs-lookup"><span data-stu-id="96697-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="96697-113">Los punteros tienen un tamaño de 4 en entornos de 32 bits y 8 en entornos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="96697-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="96697-114">Un tipo compuesto está alineado de forma natural si cada uno de sus componentes está alineado de forma natural con respecto al principio del tipo y si no hay ningún hueco (relleno) innecesario entre los componentes.</span><span class="sxs-lookup"><span data-stu-id="96697-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="96697-115">Los componentes compuestos, como campos o elementos, se recorren en componentes de puntero o de tipo base.</span><span class="sxs-lookup"><span data-stu-id="96697-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="96697-116">Una regla sencilla para ayudar a recordar este comportamiento es que la alineación natural de un tipo es igual a las alineaciones más importantes de sus componentes.</span><span class="sxs-lookup"><span data-stu-id="96697-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="96697-117">Existe una conexión entre la alineación y el tamaño de la memoria de un tipo en lenguajes como C o C++ y IDL, tal y como se expresa en el operador **sizeof ()**.</span><span class="sxs-lookup"><span data-stu-id="96697-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="96697-118">El tamaño es un múltiplo de la alineación (el múltiplo mínimo que abarca el tipo).</span><span class="sxs-lookup"><span data-stu-id="96697-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="96697-119">Esto sigue a partir de una representación de matriz en la memoria.</span><span class="sxs-lookup"><span data-stu-id="96697-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="96697-120">La alineación natural es importante porque el acceso a los datos desalineados puede producir una excepción en algunos sistemas.</span><span class="sxs-lookup"><span data-stu-id="96697-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="96697-121">Los datos se pueden marcar para una manipulación segura cuando están mal alineados, pero normalmente esto implica una penalización de velocidad que puede ser considerable en algunas plataformas.</span><span class="sxs-lookup"><span data-stu-id="96697-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="96697-122">En la memoria, se garantiza que los objetos de tipos con una alineación natural de *n* se alineen correctamente cuando se colocan en direcciones que son un múltiplo de *n*.</span><span class="sxs-lookup"><span data-stu-id="96697-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="96697-123">Empaquetado frente a alineación</span><span class="sxs-lookup"><span data-stu-id="96697-123">Packing versus Alignment</span></span>

<span data-ttu-id="96697-124">Si se especifica un nivel de empaquetado mayor que la alineación natural de un tipo, no se cambia la alineación del tipo.</span><span class="sxs-lookup"><span data-stu-id="96697-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="96697-125">La especificación de un nivel de empaquetado menor que la alineación natural reduce la alineación del tipo al nivel de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="96697-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="96697-126">Como resultado, los tipos empaquetados se pueden colocar en la memoria en direcciones que son un múltiplo del nivel de empaquetado (la alineación reducida) sin causar una falta de alineación.</span><span class="sxs-lookup"><span data-stu-id="96697-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="96697-127">Esto afecta a los tipos simples y a los tipos de componentes.</span><span class="sxs-lookup"><span data-stu-id="96697-127">This affects both simple types and component types.</span></span> <span data-ttu-id="96697-128">En el caso de los tipos compuestos, el diseño interno del tipo puede verse afectado, ya que la alineación reducida de los componentes puede cambiar el tamaño de relleno necesario para la alineación adecuada de los componentes, lo que reduce el tamaño del tipo.</span><span class="sxs-lookup"><span data-stu-id="96697-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="96697-129">Una regla sencilla para ayudar a recordar este comportamiento es que la nueva alineación de un tipo empaquetado es el menor del nivel de empaquetado y su alineación natural.</span><span class="sxs-lookup"><span data-stu-id="96697-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="96697-130">El tamaño del tipo es un múltiplo de la nueva alineación.</span><span class="sxs-lookup"><span data-stu-id="96697-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="96697-131">El operador **sizeof ()** devuelve el tamaño reducido de los tipos empaquetados.</span><span class="sxs-lookup"><span data-stu-id="96697-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="96697-132">Por ejemplo, con el nivel 2 de empaquetado se alinea a la 2 y, por lo tanto, se puede colocar en cualquier dirección, no solo en las direcciones que son un múltiplo de 4, como sucede con la alineación natural.</span><span class="sxs-lookup"><span data-stu-id="96697-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="96697-133">Una estructura con un valor Short y Long, empaquetada en 2, no necesita la separación interna entre el corto y el tiempo siguiente que fue necesario para la alineación natural; por lo tanto, no solo la estructura se alinea ahora en 2, sino que también se reduce el tamaño de 8 a 6.</span><span class="sxs-lookup"><span data-stu-id="96697-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="96697-134">Como ejemplo, considere un tipo compuesto compuesto por un carácter de 1 byte, un entero de 4 bytes de longitud y un carácter de 1 byte:</span><span class="sxs-lookup"><span data-stu-id="96697-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="96697-135">Esta estructura se alinea de forma natural en 4 y tiene el tamaño natural de 12.</span><span class="sxs-lookup"><span data-stu-id="96697-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="96697-136">En el nivel de empaquetado 4 o superior, **la estructura se** alinea en 4 y `sizeof(struct mystructtype)` es igual a 12.</span><span class="sxs-lookup"><span data-stu-id="96697-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="96697-137">La estructura no se alineará correctamente si se encuentra en la memoria en una dirección que no sea múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="96697-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="96697-138">Para el nivel de empaquetado 2, la estructura se alinea en 2 y su tamaño es 8.</span><span class="sxs-lookup"><span data-stu-id="96697-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="96697-139">La estructura empaquetada con el nivel 2 se alineará incorrectamente si se encuentra en la memoria en una dirección que no sea múltiplo de 2.</span><span class="sxs-lookup"><span data-stu-id="96697-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="96697-140">Para el nivel de empaquetado 1, la estructura se alinea en 1 y su tamaño es 6.</span><span class="sxs-lookup"><span data-stu-id="96697-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="96697-141">La estructura empaquetada con el nivel 1 se puede colocar en cualquier parte sin que se produzca un error de alineación.</span><span class="sxs-lookup"><span data-stu-id="96697-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96697-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96697-142">Related topics</span></span>

<dl> <span data-ttu-id="96697-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="96697-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="96697-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="96697-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="96697-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="96697-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 