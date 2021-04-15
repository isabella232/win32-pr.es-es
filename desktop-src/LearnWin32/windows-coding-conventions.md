---
title: Convenciones de codificación de Windows
description: Si no está familiarizado con la programación de Windows, puede estar desconcertado cuando vea por primera vez un programa de Windows.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676355"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="2877a-103">Convenciones de codificación de Windows</span><span class="sxs-lookup"><span data-stu-id="2877a-103">Windows Coding Conventions</span></span>

<span data-ttu-id="2877a-104">Si no está familiarizado con la programación de Windows, puede estar desconcertado cuando vea por primera vez un programa de Windows.</span><span class="sxs-lookup"><span data-stu-id="2877a-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="2877a-105">El código se rellena con definiciones de tipo extrañas, como **DWORD \_ ptr** y **LPRECT**, y las variables tienen nombres como *HWnd* y *pwsz* (denominado notación húngara).</span><span class="sxs-lookup"><span data-stu-id="2877a-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="2877a-106">Merece la pena dedicar un momento a aprender algunas de las convenciones de codificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="2877a-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="2877a-107">La inmensa mayoría de las API de Windows consta de funciones o interfaces del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="2877a-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="2877a-108">Muy pocas API de Windows se proporcionan como clases de C++.</span><span class="sxs-lookup"><span data-stu-id="2877a-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="2877a-109">(Una excepción significativa es GDI+, una de las API de gráficos 2D).</span><span class="sxs-lookup"><span data-stu-id="2877a-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="2877a-110">Typedefs</span><span class="sxs-lookup"><span data-stu-id="2877a-110">Typedefs</span></span>

<span data-ttu-id="2877a-111">Los encabezados de Windows contienen muchos typedefs.</span><span class="sxs-lookup"><span data-stu-id="2877a-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="2877a-112">Muchos de ellos se definen en el archivo de encabezado WinDef. h.</span><span class="sxs-lookup"><span data-stu-id="2877a-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="2877a-113">Estos son algunos de los que encontrará a menudo.</span><span class="sxs-lookup"><span data-stu-id="2877a-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="2877a-114">Tipos enteros</span><span class="sxs-lookup"><span data-stu-id="2877a-114">Integer types</span></span>



| <span data-ttu-id="2877a-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2877a-115">Data type</span></span>     | <span data-ttu-id="2877a-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2877a-116">Size</span></span>    | <span data-ttu-id="2877a-117">Conectado?</span><span class="sxs-lookup"><span data-stu-id="2877a-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="2877a-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="2877a-118">**BYTE**</span></span>      | <span data-ttu-id="2877a-119">8 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-119">8 bits</span></span>  | <span data-ttu-id="2877a-120">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-120">Unsigned</span></span> |
| <span data-ttu-id="2877a-121">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="2877a-121">**DWORD**</span></span>     | <span data-ttu-id="2877a-122">32 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-122">32 bits</span></span> | <span data-ttu-id="2877a-123">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-123">Unsigned</span></span> |
| <span data-ttu-id="2877a-124">**INT32**</span><span class="sxs-lookup"><span data-stu-id="2877a-124">**INT32**</span></span>     | <span data-ttu-id="2877a-125">32 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-125">32 bits</span></span> | <span data-ttu-id="2877a-126">Firmado</span><span class="sxs-lookup"><span data-stu-id="2877a-126">Signed</span></span>   |
| <span data-ttu-id="2877a-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="2877a-127">**INT64**</span></span>     | <span data-ttu-id="2877a-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-128">64 bits</span></span> | <span data-ttu-id="2877a-129">Firmado</span><span class="sxs-lookup"><span data-stu-id="2877a-129">Signed</span></span>   |
| <span data-ttu-id="2877a-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="2877a-130">**LONG**</span></span>      | <span data-ttu-id="2877a-131">32 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-131">32 bits</span></span> | <span data-ttu-id="2877a-132">Firmado</span><span class="sxs-lookup"><span data-stu-id="2877a-132">Signed</span></span>   |
| <span data-ttu-id="2877a-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="2877a-133">**LONGLONG**</span></span>  | <span data-ttu-id="2877a-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-134">64 bits</span></span> | <span data-ttu-id="2877a-135">Firmado</span><span class="sxs-lookup"><span data-stu-id="2877a-135">Signed</span></span>   |
| <span data-ttu-id="2877a-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2877a-136">**UINT32**</span></span>    | <span data-ttu-id="2877a-137">32 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-137">32 bits</span></span> | <span data-ttu-id="2877a-138">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-138">Unsigned</span></span> |
| <span data-ttu-id="2877a-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2877a-139">**UINT64**</span></span>    | <span data-ttu-id="2877a-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-140">64 bits</span></span> | <span data-ttu-id="2877a-141">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-141">Unsigned</span></span> |
| <span data-ttu-id="2877a-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="2877a-142">**ULONG**</span></span>     | <span data-ttu-id="2877a-143">32 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-143">32 bits</span></span> | <span data-ttu-id="2877a-144">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-144">Unsigned</span></span> |
| <span data-ttu-id="2877a-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="2877a-145">**ULONGLONG**</span></span> | <span data-ttu-id="2877a-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-146">64 bits</span></span> | <span data-ttu-id="2877a-147">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-147">Unsigned</span></span> |
| <span data-ttu-id="2877a-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="2877a-148">**WORD**</span></span>      | <span data-ttu-id="2877a-149">16 bits</span><span class="sxs-lookup"><span data-stu-id="2877a-149">16 bits</span></span> | <span data-ttu-id="2877a-150">Sin signo</span><span class="sxs-lookup"><span data-stu-id="2877a-150">Unsigned</span></span> |



 

<span data-ttu-id="2877a-151">Como puede ver, hay una cierta cantidad de redundancia en estas definiciones de nivel.</span><span class="sxs-lookup"><span data-stu-id="2877a-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="2877a-152">Algunos de estos superpuestos son simplemente debido al historial de las API de Windows.</span><span class="sxs-lookup"><span data-stu-id="2877a-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="2877a-153">Los tipos enumerados aquí tienen un tamaño fijo y los tamaños son los mismos en las aplicaciones 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="2877a-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="2877a-154">Por ejemplo, el tipo **DWORD** tiene siempre 32 bits de ancho.</span><span class="sxs-lookup"><span data-stu-id="2877a-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="2877a-155">Tipo booleano</span><span class="sxs-lookup"><span data-stu-id="2877a-155">Boolean Type</span></span>

<span data-ttu-id="2877a-156">**Bool** es una definición de tipo para un valor entero que se utiliza en un contexto booleano.</span><span class="sxs-lookup"><span data-stu-id="2877a-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="2877a-157">El archivo de encabezado WinDef. h también define dos valores para su uso con **bool**.</span><span class="sxs-lookup"><span data-stu-id="2877a-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="2877a-158">A pesar de esta definición de **true**, sin embargo, la mayoría de las funciones que devuelven un tipo **bool** pueden devolver cualquier valor distinto de cero para indicar su veracidad booleana.</span><span class="sxs-lookup"><span data-stu-id="2877a-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="2877a-159">Por lo tanto, siempre debe escribir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2877a-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="2877a-160">y no esto:</span><span class="sxs-lookup"><span data-stu-id="2877a-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="2877a-161">Tenga en cuenta que **bool** es un tipo entero y no es intercambiable con el tipo **bool** de C++.</span><span class="sxs-lookup"><span data-stu-id="2877a-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="2877a-162">Tipos de puntero</span><span class="sxs-lookup"><span data-stu-id="2877a-162">Pointer Types</span></span>

<span data-ttu-id="2877a-163">Windows define muchos tipos de datos con el formato *Pointer-to-X*.</span><span class="sxs-lookup"><span data-stu-id="2877a-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="2877a-164">Normalmente tienen el prefijo *P* o *LP* en el nombre.</span><span class="sxs-lookup"><span data-stu-id="2877a-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="2877a-165">Por ejemplo, **LPRECT** es un puntero a un [**Rect**](/previous-versions//dd162897(v=vs.85)), donde **Rect** es una estructura que describe un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2877a-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="2877a-166">Las siguientes declaraciones de variable son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="2877a-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="2877a-167">Históricamente, *P* significa "Pointer" y *LP* representa el "puntero largo".</span><span class="sxs-lookup"><span data-stu-id="2877a-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="2877a-168">Los punteros largos (también denominados *punteros Far*) son un Holdover de Windows de 16 bits, cuando eran necesarios para direccionar los intervalos de memoria fuera del segmento actual.</span><span class="sxs-lookup"><span data-stu-id="2877a-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="2877a-169">El prefijo *LP* se ha conservado para facilitar el traslado del código de 16 bits a Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2877a-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="2877a-170">Actualmente no hay ninguna distinción: un puntero es un puntero.</span><span class="sxs-lookup"><span data-stu-id="2877a-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="2877a-171">Tipos de precisión del puntero</span><span class="sxs-lookup"><span data-stu-id="2877a-171">Pointer Precision Types</span></span>

<span data-ttu-id="2877a-172">Los siguientes tipos de datos siempre son el tamaño de un puntero, es decir, 32 bits de ancho en aplicaciones de 32 bits y 64 bits de ancho en aplicaciones de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2877a-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="2877a-173">El tamaño se determina en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="2877a-173">The size is determined at compile time.</span></span> <span data-ttu-id="2877a-174">Cuando una aplicación de 32 bits se ejecuta en Windows de 64 bits, estos tipos de datos siguen siendo 4 bytes de ancho.</span><span class="sxs-lookup"><span data-stu-id="2877a-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="2877a-175">(Una aplicación de 64 bits no se puede ejecutar en Windows de 32 bits, por lo que no se produce la situación inversa).</span><span class="sxs-lookup"><span data-stu-id="2877a-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="2877a-176">**DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2877a-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="2877a-177">**INT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2877a-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="2877a-178">**LONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2877a-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="2877a-179">**ULONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2877a-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="2877a-180">**UINT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2877a-180">**UINT\_PTR**</span></span>

<span data-ttu-id="2877a-181">Estos tipos se utilizan en situaciones en las que un entero podría convertirse en un puntero.</span><span class="sxs-lookup"><span data-stu-id="2877a-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="2877a-182">También se usan para definir variables para la aritmética de puntero y para definir contadores de bucle que recorren en iteración el intervalo completo de bytes en los búferes de memoria.</span><span class="sxs-lookup"><span data-stu-id="2877a-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="2877a-183">En general, aparecen en lugares donde un valor existente de 32 bits se expandió a 64 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2877a-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="2877a-184">Notación húngara</span><span class="sxs-lookup"><span data-stu-id="2877a-184">Hungarian Notation</span></span>

<span data-ttu-id="2877a-185">La *notación húngara* es la práctica de agregar prefijos a los nombres de variables, para proporcionar información adicional sobre la variable.</span><span class="sxs-lookup"><span data-stu-id="2877a-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="2877a-186">(El inventoro de la notación, Charles Simonyi, era húngaro, es decir, su nombre).</span><span class="sxs-lookup"><span data-stu-id="2877a-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="2877a-187">En su forma original, la notación húngara proporciona información *semántica* sobre una variable, que indica el uso previsto.</span><span class="sxs-lookup"><span data-stu-id="2877a-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="2877a-188">Por ejemplo, *i* es un índice, *CB* significa un tamaño en bytes ("recuento de bytes") y los números de filas y columnas de *la media de la columna y* *RW* .</span><span class="sxs-lookup"><span data-stu-id="2877a-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="2877a-189">Estos prefijos están diseñados para evitar el uso accidental de una variable en el contexto equivocado.</span><span class="sxs-lookup"><span data-stu-id="2877a-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="2877a-190">Por ejemplo, si vio la expresión `rwPosition +  cbTable` , sabrá que se está agregando un número de fila a un tamaño, lo que es casi seguro un error en el código.</span><span class="sxs-lookup"><span data-stu-id="2877a-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="2877a-191">Una forma más común de notación húngara usa prefijos para proporcionar información de *tipos* , por ejemplo, *DW* para **DWORD** y *w* para **Word**.</span><span class="sxs-lookup"><span data-stu-id="2877a-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="2877a-192">Si busca en la web "notación húngara", encontrará una gran cantidad de opiniones sobre si la notación húngara es buena o mala.</span><span class="sxs-lookup"><span data-stu-id="2877a-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="2877a-193">Algunos programadores tienen una intensa diferencia en la notación húngara.</span><span class="sxs-lookup"><span data-stu-id="2877a-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="2877a-194">Otros lo encuentran útiles.</span><span class="sxs-lookup"><span data-stu-id="2877a-194">Others find it helpful.</span></span> <span data-ttu-id="2877a-195">Sin embargo, muchos de los ejemplos de código de MSDN usan la notación húngara, pero no es necesario memorizar los prefijos para comprender el código.</span><span class="sxs-lookup"><span data-stu-id="2877a-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="2877a-196">Siguientes</span><span class="sxs-lookup"><span data-stu-id="2877a-196">Next</span></span>

[<span data-ttu-id="2877a-197">Trabajar con cadenas</span><span class="sxs-lookup"><span data-stu-id="2877a-197">Working with Strings</span></span>](working-with-strings.md)

 

 