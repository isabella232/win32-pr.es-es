---
title: Las herramientas
description: En este tema se describen las herramientas disponibles para su uso a fin de que la aplicación esté preparada para 64 bits. Windows 10 está disponible para procesadores basados en x64 y en ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, herramientas
- herramientas de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418992"
---
# <a name="the-tools"></a><span data-ttu-id="c2460-106">Las herramientas</span><span class="sxs-lookup"><span data-stu-id="c2460-106">The Tools</span></span>

<span data-ttu-id="c2460-107">En este tema se describen las herramientas disponibles para su uso a fin de que la aplicación esté preparada para 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="c2460-108">Windows 10 está disponible para procesadores basados en x64 y en ARM64.</span><span class="sxs-lookup"><span data-stu-id="c2460-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="c2460-109">Archivos de inclusión</span><span class="sxs-lookup"><span data-stu-id="c2460-109">Include Files</span></span>

<span data-ttu-id="c2460-110">Los elementos de la API son prácticamente idénticos entre las ventanas 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="c2460-111">Los archivos de encabezado de Windows se han modificado de modo que se puedan usar para el código de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="c2460-112">Los nuevos tipos de 64 bits y macros se definen en un nuevo archivo de encabezado, Basetsd. h, que se encuentra en el conjunto de archivos de encabezado incluidos en Windows. h.</span><span class="sxs-lookup"><span data-stu-id="c2460-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="c2460-113">Basetsd. h incluye las nuevas definiciones de tipos de datos para ayudar a que el código fuente tenga un tamaño de texto independiente.</span><span class="sxs-lookup"><span data-stu-id="c2460-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="c2460-114">Nuevos tipos de datos</span><span class="sxs-lookup"><span data-stu-id="c2460-114">New Data Types</span></span>

<span data-ttu-id="c2460-115">Los archivos de encabezado de Windows contienen nuevos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="c2460-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="c2460-116">Estos tipos son principalmente para la compatibilidad de tipos con los tipos de datos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="c2460-117">Los nuevos tipos proporcionan exactamente el mismo tipo que los tipos existentes, al mismo tiempo que proporcionan compatibilidad para Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="c2460-118">Para obtener más información, vea [los nuevos tipos de datos](the-new-data-types.md) o el archivo de encabezado Basetsd. h.</span><span class="sxs-lookup"><span data-stu-id="c2460-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="c2460-119">Macros predefinidas</span><span class="sxs-lookup"><span data-stu-id="c2460-119">Predefined Macros</span></span>

<span data-ttu-id="c2460-120">El compilador define las macros siguientes para identificar la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c2460-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="c2460-121">Macro</span><span class="sxs-lookup"><span data-stu-id="c2460-121">Macro</span></span>   | <span data-ttu-id="c2460-122">Significado</span><span class="sxs-lookup"><span data-stu-id="c2460-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2460-123">\_WIN64</span><span class="sxs-lookup"><span data-stu-id="c2460-123">\_WIN64</span></span> | <span data-ttu-id="c2460-124">Plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-124">A 64-bit platform.</span></span> <span data-ttu-id="c2460-125">Esto incluye tanto x64 como ARM64.</span><span class="sxs-lookup"><span data-stu-id="c2460-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="c2460-126">\_32</span><span class="sxs-lookup"><span data-stu-id="c2460-126">\_WIN32</span></span> | <span data-ttu-id="c2460-127">Plataforma de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-127">A 32-bit platform.</span></span> <span data-ttu-id="c2460-128">Este valor también lo define el compilador de 64 bits para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c2460-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="c2460-129">\_WIN16</span><span class="sxs-lookup"><span data-stu-id="c2460-129">\_WIN16</span></span> | <span data-ttu-id="c2460-130">Una plataforma de 16 bits</span><span class="sxs-lookup"><span data-stu-id="c2460-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="c2460-131">Las macros siguientes son específicas de la arquitectura.</span><span class="sxs-lookup"><span data-stu-id="c2460-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="c2460-132">Macro</span><span class="sxs-lookup"><span data-stu-id="c2460-132">Macro</span></span>      | <span data-ttu-id="c2460-133">Significado</span><span class="sxs-lookup"><span data-stu-id="c2460-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="c2460-134">\_M \_ ia64</span><span class="sxs-lookup"><span data-stu-id="c2460-134">\_M\_IA64</span></span>  | <span data-ttu-id="c2460-135">Plataforma Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="c2460-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="c2460-136">\_M \_ IX86</span><span class="sxs-lookup"><span data-stu-id="c2460-136">\_M\_IX86</span></span>  | <span data-ttu-id="c2460-137">plataforma x86</span><span class="sxs-lookup"><span data-stu-id="c2460-137">x86 platform</span></span>           |
| <span data-ttu-id="c2460-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="c2460-138">\_M\_X64</span></span>   | <span data-ttu-id="c2460-139">plataforma x64</span><span class="sxs-lookup"><span data-stu-id="c2460-139">x64 platform</span></span>           |
| <span data-ttu-id="c2460-140">\_M \_ ARM64</span><span class="sxs-lookup"><span data-stu-id="c2460-140">\_M\_ARM64</span></span> | <span data-ttu-id="c2460-141">Plataforma ARM64</span><span class="sxs-lookup"><span data-stu-id="c2460-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="c2460-142">No utilice estas macros excepto con código específico de la arquitectura, en su lugar, use \_ WIN64, \_ Win32 y \_ WIN16 siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="c2460-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="c2460-143">Funciones del asistente</span><span class="sxs-lookup"><span data-stu-id="c2460-143">Helper Functions</span></span>

<span data-ttu-id="c2460-144">Las siguientes funciones insertadas (definidas en Basetsd. h) pueden ayudarle a convertir los valores de un tipo a otro de forma segura.</span><span class="sxs-lookup"><span data-stu-id="c2460-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="c2460-145">El signo de **IntToPtr** extiende el valor **int** , **UIntToPtr** cero: extiende el valor **int sin signo** , **LongToPtr** el signo y extiende el valor **Long** , y **ULongToPtr** cero extiende el valor **Long sin signo** .</span><span class="sxs-lookup"><span data-stu-id="c2460-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="c2460-146">compilador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c2460-146">64-bit Compiler</span></span>

<span data-ttu-id="c2460-147">Los compiladores de 64 bits se pueden usar para identificar el truncamiento de punteros, conversiones de tipos incorrectas y otros problemas específicos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="c2460-148">Cuando se ejecuta el compilador por primera vez, es probable que genere muchas advertencias de truncamiento de puntero o de falta de coincidencia de tipos, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2460-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="c2460-149">Use estas advertencias como guía para hacer que el código sea más sólido.</span><span class="sxs-lookup"><span data-stu-id="c2460-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="c2460-150">Se recomienda eliminar todas las advertencias, especialmente las advertencias de truncamiento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c2460-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="c2460-151">Advertencias y modificadores de compilador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c2460-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="c2460-152">Tenga en cuenta que este compilador habilita el modelo de datos LLP64.</span><span class="sxs-lookup"><span data-stu-id="c2460-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="c2460-153">Existe una opción de advertencia para ayudar a migrar a LLP64.</span><span class="sxs-lookup"><span data-stu-id="c2460-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="c2460-154">El modificador-Wp64-W3 habilita las siguientes advertencias:</span><span class="sxs-lookup"><span data-stu-id="c2460-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="c2460-155">C4305: ADVERTENCIA de truncamiento.</span><span class="sxs-lookup"><span data-stu-id="c2460-155">C4305: Truncation warning.</span></span> <span data-ttu-id="c2460-156">Por ejemplo, "Return": truncamiento de "unsigned Int64" a "Long".</span><span class="sxs-lookup"><span data-stu-id="c2460-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="c2460-157">C4311: ADVERTENCIA de truncamiento.</span><span class="sxs-lookup"><span data-stu-id="c2460-157">C4311: Truncation warning.</span></span> <span data-ttu-id="c2460-158">Por ejemplo, "tipo de conversión": truncamiento de puntero de "int \* \_ ptr64" a "int".</span><span class="sxs-lookup"><span data-stu-id="c2460-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="c2460-159">C4312: conversión a una advertencia de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="c2460-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="c2460-160">Por ejemplo, "tipo de conversión": conversión de "int" a "int \* \_ ptr64" de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="c2460-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="c2460-161">C4318: pasando longitud cero.</span><span class="sxs-lookup"><span data-stu-id="c2460-161">C4318: Passing zero length.</span></span> <span data-ttu-id="c2460-162">Por ejemplo, pasar la constante Zero como longitud a la función **memset** .</span><span class="sxs-lookup"><span data-stu-id="c2460-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="c2460-163">C4319: operador not.</span><span class="sxs-lookup"><span data-stu-id="c2460-163">C4319: Not operator.</span></span> <span data-ttu-id="c2460-164">Por ejemplo, "~": extensión de cero "unsigned Long" a "Int64 sin signo \_ " de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="c2460-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="c2460-165">C4313: llamar a la familia de funciones **printf** con especificadores y argumentos de tipo de conversión conflictivos.</span><span class="sxs-lookup"><span data-stu-id="c2460-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="c2460-166">Por ejemplo, "printf": "% p" en la cadena de formato entra en conflicto con el argumento 2 de tipo " \_ Int64".</span><span class="sxs-lookup"><span data-stu-id="c2460-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="c2460-167">Otro ejemplo es la llamada a printf ("% x", el valor del puntero \_ ); esto provoca un truncamiento de los 32 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="c2460-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="c2460-168">La llamada correcta es printf ("% p", valor de puntero \_ ).</span><span class="sxs-lookup"><span data-stu-id="c2460-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="c2460-169">C4244: igual que el C4242 de advertencia existente.</span><span class="sxs-lookup"><span data-stu-id="c2460-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="c2460-170">Por ejemplo, "Return": conversión de " \_ Int64" a "int sin signo", posible pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="c2460-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="c2460-171">Enlazador y bibliotecas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c2460-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="c2460-172">Para compilar aplicaciones, use el enlazador y las bibliotecas proporcionadas por el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c2460-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="c2460-173">La mayoría de las bibliotecas de 32 bits tienen una versión de 64 bits correspondiente, pero algunas bibliotecas heredadas solo están disponibles en las versiones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="c2460-174">El código que llama a estas bibliotecas no se vinculará cuando la aplicación se compile para Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2460-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





