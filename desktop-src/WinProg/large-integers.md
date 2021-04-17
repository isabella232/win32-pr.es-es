---
title: Enteros grandes
description: Las estructuras y funciones de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en Windows de 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- enteros grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705015"
---
# <a name="large-integers"></a><span data-ttu-id="6050b-104">Enteros grandes</span><span class="sxs-lookup"><span data-stu-id="6050b-104">Large Integers</span></span>

<span data-ttu-id="6050b-105">Las estructuras y funciones de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6050b-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="6050b-106">Ahora, el compilador de C puede admitir enteros de 64 bits de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="6050b-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="6050b-107">Por ejemplo, Microsoft Visual C++ admite el tipo de entero con tamaño [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="6050b-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="6050b-108">Para obtener más información, vea la documentación incluida en el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="6050b-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="6050b-109">Para obtener información sobre los enteros de 64 bits en Windows de 64 bits, consulte [los nuevos tipos de datos](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="6050b-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="6050b-110">Operaciones de enteros grandes</span><span class="sxs-lookup"><span data-stu-id="6050b-110">Large Integer Operations</span></span>

<span data-ttu-id="6050b-111">Las aplicaciones pueden multiplicar enteros de 32 bits con signo o sin signo, generando resultados de 64 bits, mediante las funciones [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) y [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="6050b-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="6050b-112">Las aplicaciones pueden cambiar los bits de los valores de 64 bits a la izquierda o a la derecha mediante las funciones [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)y [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) .</span><span class="sxs-lookup"><span data-stu-id="6050b-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="6050b-113">Estas funciones proporcionan el desplazamiento aritmético y lógico.</span><span class="sxs-lookup"><span data-stu-id="6050b-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="6050b-114">Las aplicaciones también pueden multiplicar y dividir los valores de 32 bits en una sola operación mediante la función [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) .</span><span class="sxs-lookup"><span data-stu-id="6050b-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="6050b-115">Aunque el resultado de la operación es un valor de 32 bits, la función almacena el resultado intermedio como un valor de 64 bits, de modo que la información no se pierde cuando se multiplican y dividen valores grandes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6050b-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="6050b-116">Referencia de entero grande</span><span class="sxs-lookup"><span data-stu-id="6050b-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="6050b-117">Funciones de enteros grandes</span><span class="sxs-lookup"><span data-stu-id="6050b-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="6050b-118">Estructuras de enteros grandes</span><span class="sxs-lookup"><span data-stu-id="6050b-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 