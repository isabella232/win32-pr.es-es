---
title: Sugerencias de migración
description: Es importante tener en cuenta los cálculos de direcciones y la aritmética de punteros al trasladar el código a Windows de 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, sugerencias de migración
- sugerencias para la migración de 64 bits programación de Windows
- compatibilidad con la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777245"
---
# <a name="migration-tips"></a><span data-ttu-id="4d6d6-106">Sugerencias de migración</span><span class="sxs-lookup"><span data-stu-id="4d6d6-106">Migration Tips</span></span>

<span data-ttu-id="4d6d6-107">Las dos áreas principales de preocupación al examinar el código para la compatibilidad con 64 bits son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4d6d6-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="4d6d6-108">Cálculos de direcciones</span><span class="sxs-lookup"><span data-stu-id="4d6d6-108">Address calculations</span></span>
-   <span data-ttu-id="4d6d6-109">Aritmética de puntero</span><span class="sxs-lookup"><span data-stu-id="4d6d6-109">Pointer arithmetic</span></span>

<span data-ttu-id="4d6d6-110">Por muchas razones, los desarrolladores han almacenado direcciones como un valor **ULong** .</span><span class="sxs-lookup"><span data-stu-id="4d6d6-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="4d6d6-111">Después de todo, en Windows de 32 bits, una dirección, un puntero y un valor **ULong** tienen una longitud de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4d6d6-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="4d6d6-112">Sin embargo, en Windows de 64 bits, una dirección y un **ULong** no tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="4d6d6-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="4d6d6-113">Mientras que **ULong** sigue siendo un valor de 32 bits, todos los punteros son ahora valores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4d6d6-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4d6d6-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4d6d6-114">In this Section</span></span>

-   [<span data-ttu-id="4d6d6-115">Instrucciones generales de portabilidad</span><span class="sxs-lookup"><span data-stu-id="4d6d6-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="4d6d6-116">Almacenar un valor de 64 bits</span><span class="sxs-lookup"><span data-stu-id="4d6d6-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="4d6d6-117">Errores comunes del compilador</span><span class="sxs-lookup"><span data-stu-id="4d6d6-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="4d6d6-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="4d6d6-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




