---
title: Control de errores en COM (introducción a Win32 y C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685810"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="6fab9-103">Control de errores en COM (introducción a Win32 y C++)</span><span class="sxs-lookup"><span data-stu-id="6fab9-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="6fab9-104">COM utiliza valores **HRESULT** para indicar si la llamada a un método o una función se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6fab9-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="6fab9-105">Varios encabezados de SDK definen varias constantes de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fab9-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="6fab9-106">En WinError. h se define un conjunto común de códigos para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="6fab9-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="6fab9-107">En la tabla siguiente se muestran algunos de los códigos de retorno para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="6fab9-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="6fab9-108">Constante</span><span class="sxs-lookup"><span data-stu-id="6fab9-108">Constant</span></span>            | <span data-ttu-id="6fab9-109">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="6fab9-109">Numeric value</span></span> | <span data-ttu-id="6fab9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fab9-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="6fab9-111">**E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="6fab9-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="6fab9-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="6fab9-112">0x80070005</span></span>    | <span data-ttu-id="6fab9-113">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="6fab9-113">Access denied.</span></span>                                       |
| <span data-ttu-id="6fab9-114">**E \_ FAIL**</span><span class="sxs-lookup"><span data-stu-id="6fab9-114">**E\_FAIL**</span></span>         | <span data-ttu-id="6fab9-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="6fab9-115">0x80004005</span></span>    | <span data-ttu-id="6fab9-116">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="6fab9-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="6fab9-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="6fab9-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="6fab9-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="6fab9-118">0x80070057</span></span>    | <span data-ttu-id="6fab9-119">Valor de parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6fab9-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="6fab9-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="6fab9-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="6fab9-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="6fab9-121">0x8007000E</span></span>    | <span data-ttu-id="6fab9-122">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6fab9-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="6fab9-123">**\_puntero E**</span><span class="sxs-lookup"><span data-stu-id="6fab9-123">**E\_POINTER**</span></span>      | <span data-ttu-id="6fab9-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="6fab9-124">0x80004003</span></span>    | <span data-ttu-id="6fab9-125">Se pasó incorrectamente **null** para un valor de puntero.</span><span class="sxs-lookup"><span data-stu-id="6fab9-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="6fab9-126">**E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="6fab9-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="6fab9-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="6fab9-127">0x8000FFFF</span></span>    | <span data-ttu-id="6fab9-128">Condición inesperada.</span><span class="sxs-lookup"><span data-stu-id="6fab9-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="6fab9-129">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="6fab9-129">**S\_OK**</span></span>           | <span data-ttu-id="6fab9-130">0x0</span><span class="sxs-lookup"><span data-stu-id="6fab9-130">0x0</span></span>           | <span data-ttu-id="6fab9-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6fab9-131">Success.</span></span>                                             |
| <span data-ttu-id="6fab9-132">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="6fab9-132">**S\_FALSE**</span></span>        | <span data-ttu-id="6fab9-133">0x1</span><span class="sxs-lookup"><span data-stu-id="6fab9-133">0x1</span></span>           | <span data-ttu-id="6fab9-134">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6fab9-134">Success.</span></span>                                             |



 

<span data-ttu-id="6fab9-135">Todas las constantes con el prefijo "E \_ " son códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6fab9-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="6fab9-136">Las constantes **S \_ OK** y **s \_ false** son códigos correctos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="6fab9-137">Probablemente, el 99% de los métodos COM devuelven los elementos **\_ correctos** cuando se ejecutan correctamente, pero no le informan de este hecho.</span><span class="sxs-lookup"><span data-stu-id="6fab9-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="6fab9-138">Un método puede devolver otros códigos correctos, por lo que siempre se comprueba si hay errores mediante la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) o [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="6fab9-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="6fab9-139">En el ejemplo de código siguiente se muestra la manera equivocada y la manera correcta de comprobar si la llamada a una función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="6fab9-140">El código de operación correcta **S \_ false** merece mención.</span><span class="sxs-lookup"><span data-stu-id="6fab9-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="6fab9-141">Algunos métodos usan **S \_ false** para indicar, aproximadamente, una condición negativa que no es un error.</span><span class="sxs-lookup"><span data-stu-id="6fab9-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="6fab9-142">También puede indicar un "no operativo": el método se realizó correctamente, pero no tenía ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="6fab9-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="6fab9-143">Por ejemplo, la función [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) devuelve **S \_ false** si se llama por segunda vez desde el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="6fab9-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="6fab9-144">Si necesita diferenciar entre **s \_ OK** y **s \_ false** en el código, debe probar el valor directamente, pero seguir usando [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) o [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) para administrar los casos restantes, tal como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="6fab9-145">Algunos valores **HRESULT** son específicos de una determinada característica o subsistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="6fab9-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="6fab9-146">Por ejemplo, la API de gráficos de Direct2D define el código de error **D2DERR \_ \_ \_ formato de píxel no admitido**, lo que significa que el programa usó un formato de píxel no admitido.</span><span class="sxs-lookup"><span data-stu-id="6fab9-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="6fab9-147">La documentación de MSDN suele proporcionar una lista de códigos de error específicos que un método puede devolver.</span><span class="sxs-lookup"><span data-stu-id="6fab9-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="6fab9-148">Sin embargo, no debe considerar que estas listas sean definitivas.</span><span class="sxs-lookup"><span data-stu-id="6fab9-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="6fab9-149">Un método siempre puede devolver un valor **HRESULT** que no aparece en la documentación.</span><span class="sxs-lookup"><span data-stu-id="6fab9-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="6fab9-150">De nuevo, use las macros [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="6fab9-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="6fab9-151">Si comprueba un código de error específico, incluya también un caso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6fab9-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="6fab9-152">Patrones para el control de errores</span><span class="sxs-lookup"><span data-stu-id="6fab9-152">Patterns for Error Handling</span></span>

<span data-ttu-id="6fab9-153">En esta sección se examinan algunos patrones para controlar los errores de COM de una manera estructurada.</span><span class="sxs-lookup"><span data-stu-id="6fab9-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="6fab9-154">Cada patrón tiene ventajas y desventajas.</span><span class="sxs-lookup"><span data-stu-id="6fab9-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="6fab9-155">En cierta medida, la elección es una cuestión de sabor.</span><span class="sxs-lookup"><span data-stu-id="6fab9-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="6fab9-156">Si trabaja en un proyecto existente, es posible que ya tenga instrucciones de codificación que propongan un estilo determinado.</span><span class="sxs-lookup"><span data-stu-id="6fab9-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="6fab9-157">Independientemente del modelo que adopte, el código sólido obedecerá las siguientes reglas.</span><span class="sxs-lookup"><span data-stu-id="6fab9-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="6fab9-158">Para cada método o función que devuelva un **HRESULT**, compruebe el valor devuelto antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="6fab9-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="6fab9-159">Libere recursos después de usarlos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="6fab9-160">No intente obtener acceso a recursos no válidos o no inicializados, como punteros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="6fab9-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="6fab9-161">No intente usar un recurso después de liberarlo.</span><span class="sxs-lookup"><span data-stu-id="6fab9-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="6fab9-162">Teniendo en cuenta estas reglas, aquí hay cuatro patrones para controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="6fab9-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="6fab9-163">IFS anidado</span><span class="sxs-lookup"><span data-stu-id="6fab9-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="6fab9-164">IFS en cascada</span><span class="sxs-lookup"><span data-stu-id="6fab9-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="6fab9-165">Error de salto</span><span class="sxs-lookup"><span data-stu-id="6fab9-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="6fab9-166">Iniciar en error</span><span class="sxs-lookup"><span data-stu-id="6fab9-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="6fab9-167">IFS anidado</span><span class="sxs-lookup"><span data-stu-id="6fab9-167">Nested ifs</span></span>

<span data-ttu-id="6fab9-168">Después de cada llamada que devuelve un **valor HRESULT**, use una instrucción **If** para comprobar si se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="6fab9-169">A continuación, coloque la siguiente llamada al método en el ámbito de la instrucción **If** .</span><span class="sxs-lookup"><span data-stu-id="6fab9-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="6fab9-170">Más instrucciones **If** se pueden anidar tan profundamente como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6fab9-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="6fab9-171">Todos los ejemplos de código anteriores de este módulo usan este patrón, pero aquí lo están:</span><span class="sxs-lookup"><span data-stu-id="6fab9-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="6fab9-172">Ventajas</span><span class="sxs-lookup"><span data-stu-id="6fab9-172">Advantages</span></span>

-   <span data-ttu-id="6fab9-173">Las variables se pueden declarar con el ámbito mínimo.</span><span class="sxs-lookup"><span data-stu-id="6fab9-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="6fab9-174">Por ejemplo, *pItem* no se declara hasta que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6fab9-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="6fab9-175">Dentro de cada instrucción **If** , se cumplen ciertas condiciones invariables: todas las llamadas anteriores se han realizado correctamente y todos los recursos adquiridos siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="6fab9-176">En el ejemplo anterior, cuando el programa alcanza la instrucción **If** más interna, se sabe que *pItem* y *pFileOpen* son válidos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="6fab9-177">Está claro Cuándo se deben liberar los punteros de interfaz y otros recursos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="6fab9-178">Libera un recurso al final de la instrucción **If** que sigue inmediatamente a la llamada que adquirió el recurso.</span><span class="sxs-lookup"><span data-stu-id="6fab9-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="6fab9-179">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="6fab9-179">Disadvantages</span></span>

-   <span data-ttu-id="6fab9-180">Algunas personas buscan un anidamiento profundo difícil de leer.</span><span class="sxs-lookup"><span data-stu-id="6fab9-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="6fab9-181">El control de errores se mezcla con otras instrucciones de bifurcación y bucle.</span><span class="sxs-lookup"><span data-stu-id="6fab9-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="6fab9-182">Esto puede hacer que la lógica general del programa sea más difícil de seguir.</span><span class="sxs-lookup"><span data-stu-id="6fab9-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="6fab9-183">IFS en cascada</span><span class="sxs-lookup"><span data-stu-id="6fab9-183">Cascading ifs</span></span>

<span data-ttu-id="6fab9-184">Después de cada llamada al método, use una instrucción **If** para comprobar si la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="6fab9-185">Si el método se ejecuta correctamente, coloque la siguiente llamada de método dentro del bloque **If** .</span><span class="sxs-lookup"><span data-stu-id="6fab9-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="6fab9-186">Pero en lugar de anidar más instrucciones **If** , coloque cada prueba [**correcta**](/windows/desktop/api/winerror/nf-winerror-succeeded) subsiguiente después del bloque **If** anterior.</span><span class="sxs-lookup"><span data-stu-id="6fab9-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="6fab9-187">Si se produce un error en algún método, todas las pruebas **correctas** restantes simplemente producirán un error hasta que se alcance la parte inferior de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="6fab9-188">En este patrón, libera recursos al final de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="6fab9-189">Si se produce un error, es posible que algunos punteros no sean válidos cuando la función termina.</span><span class="sxs-lookup"><span data-stu-id="6fab9-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="6fab9-190">La llamada a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en un puntero no válido bloqueará el programa (o peor), por lo que debe inicializar todos los punteros en **null** y comprobar si son **null** antes de liberarlos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="6fab9-191">En este ejemplo se utiliza la `SafeRelease` función; los punteros inteligentes también son una buena opción.</span><span class="sxs-lookup"><span data-stu-id="6fab9-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="6fab9-192">Si usa este patrón, debe tener cuidado con las construcciones de bucle.</span><span class="sxs-lookup"><span data-stu-id="6fab9-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="6fab9-193">Dentro de un bucle, interrumpa el bucle si se produce un error en cualquier llamada.</span><span class="sxs-lookup"><span data-stu-id="6fab9-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="6fab9-194">Ventajas</span><span class="sxs-lookup"><span data-stu-id="6fab9-194">Advantages</span></span>

-   <span data-ttu-id="6fab9-195">Este patrón crea menos anidamiento que el patrón "IFS anidado".</span><span class="sxs-lookup"><span data-stu-id="6fab9-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="6fab9-196">El flujo de control general es más fácil de ver.</span><span class="sxs-lookup"><span data-stu-id="6fab9-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="6fab9-197">Los recursos se liberan en un punto del código.</span><span class="sxs-lookup"><span data-stu-id="6fab9-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="6fab9-198">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="6fab9-198">Disadvantages</span></span>

-   <span data-ttu-id="6fab9-199">Todas las variables deben declararse e inicializarse en la parte superior de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="6fab9-200">Si se produce un error en una llamada, la función realiza varias comprobaciones de errores innecesarias, en lugar de salir inmediatamente de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="6fab9-201">Dado que el flujo de control continúa a través de la función después de un error, debe tener cuidado en todo el cuerpo de la función para no tener acceso a recursos no válidos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="6fab9-202">Los errores dentro de un bucle requieren un caso especial.</span><span class="sxs-lookup"><span data-stu-id="6fab9-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="6fab9-203">Error de salto</span><span class="sxs-lookup"><span data-stu-id="6fab9-203">Jump on Fail</span></span>

<span data-ttu-id="6fab9-204">Después de cada llamada al método, pruebe si hay un error (no correcto).</span><span class="sxs-lookup"><span data-stu-id="6fab9-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="6fab9-205">En caso de error, saltar a una etiqueta cerca de la parte inferior de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="6fab9-206">Después de la etiqueta, pero antes de salir de la función, libere recursos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="6fab9-207">Ventajas</span><span class="sxs-lookup"><span data-stu-id="6fab9-207">Advantages</span></span>

-   <span data-ttu-id="6fab9-208">El flujo de control general es fácil de ver.</span><span class="sxs-lookup"><span data-stu-id="6fab9-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="6fab9-209">En cada punto del código después de una comprobación con [**errores**](/windows/desktop/api/winerror/nf-winerror-failed) , si no ha saltado a la etiqueta, se garantiza que todas las llamadas anteriores se han realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="6fab9-210">Los recursos se liberan en un lugar del código.</span><span class="sxs-lookup"><span data-stu-id="6fab9-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="6fab9-211">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="6fab9-211">Disadvantages</span></span>

-   <span data-ttu-id="6fab9-212">Todas las variables deben declararse e inicializarse en la parte superior de la función.</span><span class="sxs-lookup"><span data-stu-id="6fab9-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="6fab9-213">Algunos programadores no desean usar **goto** en su código.</span><span class="sxs-lookup"><span data-stu-id="6fab9-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="6fab9-214">(Sin embargo, se debe observar que este uso de **goto** está muy estructurado; el código nunca salta fuera de la llamada de función actual).</span><span class="sxs-lookup"><span data-stu-id="6fab9-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="6fab9-215">las instrucciones **goto** omiten los inicializadores.</span><span class="sxs-lookup"><span data-stu-id="6fab9-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="6fab9-216">Iniciar en error</span><span class="sxs-lookup"><span data-stu-id="6fab9-216">Throw on Fail</span></span>

<span data-ttu-id="6fab9-217">En lugar de saltar a una etiqueta, puede producir una excepción cuando se produce un error en un método.</span><span class="sxs-lookup"><span data-stu-id="6fab9-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="6fab9-218">Esto puede generar un estilo más idiomático de C++ si se usa para escribir código seguro para excepciones.</span><span class="sxs-lookup"><span data-stu-id="6fab9-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="6fab9-219">Observe que en este ejemplo se usa la clase **CComPtr** para administrar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="6fab9-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="6fab9-220">Por lo general, si el código produce excepciones, debe seguir el patrón RAII (la adquisición de recursos es inicialización).</span><span class="sxs-lookup"><span data-stu-id="6fab9-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="6fab9-221">Es decir, cada recurso debe ser administrado por un objeto cuyo destructor garantiza que el recurso se libera correctamente.</span><span class="sxs-lookup"><span data-stu-id="6fab9-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="6fab9-222">Si se produce una excepción, se garantiza la invocación del destructor.</span><span class="sxs-lookup"><span data-stu-id="6fab9-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="6fab9-223">De lo contrario, el programa podría perder recursos.</span><span class="sxs-lookup"><span data-stu-id="6fab9-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="6fab9-224">Ventajas</span><span class="sxs-lookup"><span data-stu-id="6fab9-224">Advantages</span></span>

-   <span data-ttu-id="6fab9-225">Compatible con el código existente que usa el control de excepciones.</span><span class="sxs-lookup"><span data-stu-id="6fab9-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="6fab9-226">Es compatible con las bibliotecas de C++ que producen excepciones, como la biblioteca de plantillas estándar (STL).</span><span class="sxs-lookup"><span data-stu-id="6fab9-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="6fab9-227">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="6fab9-227">Disadvantages</span></span>

-   <span data-ttu-id="6fab9-228">Requiere objetos de C++ para administrar recursos como la memoria o los identificadores de archivo.</span><span class="sxs-lookup"><span data-stu-id="6fab9-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="6fab9-229">Requiere una buena comprensión de cómo escribir código seguro para excepciones.</span><span class="sxs-lookup"><span data-stu-id="6fab9-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="6fab9-230">Siguientes</span><span class="sxs-lookup"><span data-stu-id="6fab9-230">Next</span></span>

[<span data-ttu-id="6fab9-231">Módulo 3. Gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="6fab9-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
