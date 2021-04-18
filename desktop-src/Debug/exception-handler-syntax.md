---
description: Las \_ \_ \_ \_ palabras clave try y Except se usan para construir un controlador de excepciones basado en marcos. En el ejemplo siguiente se muestra la estructura de un controlador de excepciones.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintaxis de Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538308"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="0f584-104">Sintaxis de Exception-Handler</span><span class="sxs-lookup"><span data-stu-id="0f584-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="0f584-105">Las palabras clave **\_ \_ try** y **\_ \_ Except** se usan para construir un controlador de excepciones basado en marcos.</span><span class="sxs-lookup"><span data-stu-id="0f584-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="0f584-106">En el ejemplo siguiente se muestra la estructura de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="0f584-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="0f584-107">Tenga en cuenta que el bloque **\_ \_ try** y el bloque de controlador de excepciones requieren llaves ( {} ).</span><span class="sxs-lookup"><span data-stu-id="0f584-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="0f584-108">No se permite usar una instrucción **goto** para saltar al cuerpo de un bloque **\_ \_ try** o a un bloque de controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="0f584-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="0f584-109">Esta regla se aplica tanto a los controladores de excepciones como a los controladores de terminación.</span><span class="sxs-lookup"><span data-stu-id="0f584-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="0f584-110">El bloque **\_ \_ try** contiene el cuerpo protegido del código que el controlador de excepciones protege.</span><span class="sxs-lookup"><span data-stu-id="0f584-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="0f584-111">Una función puede tener cualquier número de controladores de excepciones, y estas instrucciones de control de excepciones se pueden anidar dentro de la misma función o en funciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="0f584-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="0f584-112">Si se produce una excepción dentro del bloque **\_ \_ try** , el sistema toma el control y comienza la búsqueda de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="0f584-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="0f584-113">Para obtener una descripción detallada de esta búsqueda, consulte [control de excepciones](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0f584-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="0f584-114">El controlador de excepciones recibe solo las excepciones que se producen dentro de un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="0f584-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="0f584-115">Esto significa que si un bloque **\_ \_ try** contiene una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , las excepciones que se producen dentro del proceso o subproceso nuevo no se envían a este controlador.</span><span class="sxs-lookup"><span data-stu-id="0f584-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="0f584-116">El sistema evalúa la expresión de filtro de cada controlador de excepciones que protege el código en el que se produjo la excepción hasta que se controla la excepción o no hay más controladores.</span><span class="sxs-lookup"><span data-stu-id="0f584-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="0f584-117">Una expresión de filtro debe evaluarse como uno de los tres valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0f584-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="0f584-118">Value</span><span class="sxs-lookup"><span data-stu-id="0f584-118">Value</span></span>                              | <span data-ttu-id="0f584-119">Significado</span><span class="sxs-lookup"><span data-stu-id="0f584-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f584-120">**\_controlador de ejecución de excepción \_**</span><span class="sxs-lookup"><span data-stu-id="0f584-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="0f584-121">El sistema transfiere el control al controlador de excepciones y la ejecución continúa en el marco de pila en el que se encuentra el controlador.</span><span class="sxs-lookup"><span data-stu-id="0f584-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="0f584-122">**EXCEPTION \_ continue \_ Search**</span><span class="sxs-lookup"><span data-stu-id="0f584-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="0f584-123">El sistema continúa buscando un controlador.</span><span class="sxs-lookup"><span data-stu-id="0f584-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0f584-124">**ejecución de excepción \_ continua \_**</span><span class="sxs-lookup"><span data-stu-id="0f584-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="0f584-125">El sistema detiene su búsqueda de un controlador y devuelve el control al punto en el que se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="0f584-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="0f584-126">Si la excepción no es continuable, se produce una excepción de excepción no **\_ \_ continuada de excepción** .</span><span class="sxs-lookup"><span data-stu-id="0f584-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="0f584-127">La expresión de filtro se evalúa en el contexto de la función en la que se encuentra el controlador de excepciones, aunque la excepción puede haberse producido en una función diferente.</span><span class="sxs-lookup"><span data-stu-id="0f584-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="0f584-128">Esto significa que la expresión de filtro puede tener acceso a las variables locales de la función.</span><span class="sxs-lookup"><span data-stu-id="0f584-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="0f584-129">Del mismo modo, el bloque de controlador de excepciones puede tener acceso a las variables locales de la función en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="0f584-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="0f584-130">Para obtener más ejemplos, vea [usar un controlador de excepciones](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="0f584-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="0f584-131">Para obtener más información sobre las expresiones de filtro y las funciones de filtro, vea [control de excepciones basado en marcos](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0f584-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
