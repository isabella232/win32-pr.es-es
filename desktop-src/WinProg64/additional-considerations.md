---
title: Consideraciones adicionales
description: Al migrar el código, tenga en cuenta los siguientes puntos.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Sugerencias de portabilidad 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105708129"
---
# <a name="additional-considerations"></a><span data-ttu-id="70e38-104">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="70e38-104">Additional Considerations</span></span>

<span data-ttu-id="70e38-105">Al migrar el código, tenga en cuenta los siguientes puntos:</span><span class="sxs-lookup"><span data-stu-id="70e38-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="70e38-106">La hipótesis siguiente ya no es válida:</span><span class="sxs-lookup"><span data-stu-id="70e38-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="70e38-107">Sin embargo, el compilador de 64 bits define \_ Win32 para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="70e38-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="70e38-108">La hipótesis siguiente ya no es válida:</span><span class="sxs-lookup"><span data-stu-id="70e38-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="70e38-109">En este caso, la cláusula else puede representar \_ Win32 o \_ WIN64.</span><span class="sxs-lookup"><span data-stu-id="70e38-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="70e38-110">Tenga cuidado con la alineación de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="70e38-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="70e38-111">La macro de **\_ alineación de tipos** devuelve los requisitos de alineación de un tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="70e38-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="70e38-112">Por ejemplo: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 en x86, 8 en procesador Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 Everywhere</span><span class="sxs-lookup"><span data-stu-id="70e38-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="70e38-113">Por ejemplo, el código de kernel tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="70e38-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="70e38-114">probablemente se debe cambiar a:</span><span class="sxs-lookup"><span data-stu-id="70e38-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="70e38-115">Las correcciones automáticas de las excepciones de alineación del modo kernel están deshabilitadas para los sistemas Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="70e38-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="70e38-116">Tenga cuidado con las operaciones NOT.</span><span class="sxs-lookup"><span data-stu-id="70e38-116">Be careful with NOT operations.</span></span> <span data-ttu-id="70e38-117">Tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70e38-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="70e38-118">El problema es que ~ (b – 1) genera "0x0000 0000 XXXX XXXX" y no "0xFFFF FFFF XXXX XXXX".</span><span class="sxs-lookup"><span data-stu-id="70e38-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="70e38-119">El compilador no lo detectará.</span><span class="sxs-lookup"><span data-stu-id="70e38-119">The compiler will not detect this.</span></span> <span data-ttu-id="70e38-120">Para solucionarlo, cambie el código de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="70e38-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="70e38-121">Tenga cuidado al realizar operaciones sin firmar y firmadas.</span><span class="sxs-lookup"><span data-stu-id="70e38-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="70e38-122">Tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70e38-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="70e38-123">El resultado es inesperadamente grande.</span><span class="sxs-lookup"><span data-stu-id="70e38-123">The result is unexpectedly large.</span></span> <span data-ttu-id="70e38-124">La regla es que si alguno de los operandos es sin signo, el resultado es sin signo.</span><span class="sxs-lookup"><span data-stu-id="70e38-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="70e38-125">En el ejemplo anterior, un se convierte en un valor sin signo, dividido por b, y el resultado almacenado en c.</span><span class="sxs-lookup"><span data-stu-id="70e38-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="70e38-126">La conversión no implica ninguna manipulación numérica.</span><span class="sxs-lookup"><span data-stu-id="70e38-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="70e38-127">Como otro ejemplo, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="70e38-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="70e38-128">El problema surge porque x es sin signo, lo que hace que toda la expresión quede sin signo.</span><span class="sxs-lookup"><span data-stu-id="70e38-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="70e38-129">Esto funciona bien a menos que y sea negativo.</span><span class="sxs-lookup"><span data-stu-id="70e38-129">This works fine unless y is negative.</span></span> <span data-ttu-id="70e38-130">En este caso, y se convierte en un valor sin signo, la expresión se evalúa usando la precisión de 32 bits, escalada y se agrega a pVar1.</span><span class="sxs-lookup"><span data-stu-id="70e38-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="70e38-131">Un número negativo sin signo de 32 bits se convierte en un número positivo de 64 bits grande, lo que da lugar a un resultado incorrecto.</span><span class="sxs-lookup"><span data-stu-id="70e38-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="70e38-132">Para solucionar este problema, declare x como un valor con signo o convierta explícitamente a **Long** en la expresión.</span><span class="sxs-lookup"><span data-stu-id="70e38-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="70e38-133">Tenga cuidado al realizar asignaciones de tamaño por etapas.</span><span class="sxs-lookup"><span data-stu-id="70e38-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="70e38-134">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="70e38-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="70e38-135">El código siguiente es incorrecto porque el compilador rellenará la estructura con 4 bytes adicionales para establecer la alineación de 8 bytes:</span><span class="sxs-lookup"><span data-stu-id="70e38-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="70e38-136">El código siguiente es correcto:</span><span class="sxs-lookup"><span data-stu-id="70e38-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="70e38-137">No pase `(HANDLE)0xFFFFFFFF` a funciones como [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span><span class="sxs-lookup"><span data-stu-id="70e38-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="70e38-138">En su lugar, use un **\_ \_ valor de identificador no válido**.</span><span class="sxs-lookup"><span data-stu-id="70e38-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="70e38-139">Use los especificadores de formato adecuados al imprimir una cadena.</span><span class="sxs-lookup"><span data-stu-id="70e38-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="70e38-140">Use% p para imprimir punteros en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="70e38-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="70e38-141">Esta es la mejor opción para los punteros de impresión.</span><span class="sxs-lookup"><span data-stu-id="70e38-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="70e38-142">Microsoft Visual C++ admite% I para imprimir datos polimórficos.</span><span class="sxs-lookup"><span data-stu-id="70e38-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="70e38-143">Visual C++ también admite% I64 para imprimir valores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="70e38-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 