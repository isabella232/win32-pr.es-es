---
description: Las \_ \_ \_ \_ palabras clave try y finally se usan para construir un controlador de finalización. En el ejemplo siguiente se muestra la estructura de un controlador de terminación.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Sintaxis de Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659555"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="3a8df-104">Sintaxis de Termination-Handler</span><span class="sxs-lookup"><span data-stu-id="3a8df-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="3a8df-105">Las palabras clave **\_ \_ try** y **\_ \_ Finally** se usan para construir un controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="3a8df-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="3a8df-106">En el ejemplo siguiente se muestra la estructura de un controlador de terminación.</span><span class="sxs-lookup"><span data-stu-id="3a8df-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="3a8df-107">Para obtener ejemplos, vea [usar un controlador de terminación](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="3a8df-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="3a8df-108">Al igual que con el controlador de excepciones, tanto el bloque **\_ \_ try** como el bloque **\_ \_ Finally** requieren llaves ( {} ), y no se permite el uso de una instrucción **goto** para saltar a cualquiera de los bloques.</span><span class="sxs-lookup"><span data-stu-id="3a8df-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="3a8df-109">El bloque **\_ \_ try** contiene el cuerpo protegido del código que está protegido por el controlador de terminación.</span><span class="sxs-lookup"><span data-stu-id="3a8df-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="3a8df-110">Una función puede tener cualquier número de controladores de terminación y estos bloques de control de terminación se pueden anidar dentro de la misma función o en funciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="3a8df-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="3a8df-111">El bloque **\_ \_ Finally** se ejecuta siempre que el flujo de control sale del bloque **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="3a8df-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="3a8df-112">Sin embargo, el bloque **\_ \_ Finally** no se ejecuta si se llama a cualquiera de las siguientes funciones en el bloque **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **Abort**.</span><span class="sxs-lookup"><span data-stu-id="3a8df-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="3a8df-113">El bloque **\_ \_ Finally** se ejecuta en el contexto de la función en la que se encuentra el controlador de terminación.</span><span class="sxs-lookup"><span data-stu-id="3a8df-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="3a8df-114">Esto significa que el bloque **\_ \_ Finally** puede tener acceso a las variables locales de la función.</span><span class="sxs-lookup"><span data-stu-id="3a8df-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="3a8df-115">La ejecución del bloque **\_ \_ Finally** puede finalizar con cualquiera de los siguientes medios.</span><span class="sxs-lookup"><span data-stu-id="3a8df-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="3a8df-116">Ejecución de la última instrucción en el bloque y continuación a la siguiente instrucción</span><span class="sxs-lookup"><span data-stu-id="3a8df-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="3a8df-117">Uso de una instrucción de control (**Return**, **break**, **continue** o **goto**)</span><span class="sxs-lookup"><span data-stu-id="3a8df-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="3a8df-118">Uso de **longjmp** o un salto a un controlador de excepciones</span><span class="sxs-lookup"><span data-stu-id="3a8df-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="3a8df-119">Si la ejecución del bloque **\_ \_ try** finaliza debido a una excepción que invoca el bloque de control de excepciones de un controlador de excepciones basado en marcos, el bloque **\_ \_ Finally** se ejecuta antes de que se ejecute el bloque de control de excepciones.</span><span class="sxs-lookup"><span data-stu-id="3a8df-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="3a8df-120">Del mismo modo, una llamada a la función de biblioteca en tiempo de ejecución de C de **longjmp** desde el bloque **\_ \_ try** produce la ejecución del bloque **\_ \_ Finally** antes de que se reanude la ejecución en el destino de la operación **longjmp** .</span><span class="sxs-lookup"><span data-stu-id="3a8df-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="3a8df-121">Si la ejecución de bloque **\_ \_ try** finaliza debido a una instrucción de control (**Return**, **break**, **continue** o **goto**), se ejecuta el bloque **\_ \_ Finally** .</span><span class="sxs-lookup"><span data-stu-id="3a8df-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="3a8df-122">La función [**AbnormalTermination**](abnormaltermination.md) se puede usar en el bloque **\_ \_ Finally** para determinar si el bloque **\_ \_ try** terminó secuencialmente, es decir, si llegó a la llave de cierre (}).</span><span class="sxs-lookup"><span data-stu-id="3a8df-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="3a8df-123">Si se deja el bloque **\_ \_ try** debido a una llamada a **longjmp**, un salto a un controlador de excepciones o una instrucción **Return**, **break**, **continue** o **goto** , se considera una terminación anómala.</span><span class="sxs-lookup"><span data-stu-id="3a8df-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="3a8df-124">Tenga en cuenta que si no se termina secuencialmente, el sistema busca en todos los marcos de pila en orden inverso para determinar si se debe llamar a algún controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="3a8df-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="3a8df-125">Esto puede producir una degradación del rendimiento debido a la ejecución de cientos de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="3a8df-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="3a8df-126">Para evitar la terminación anómala del controlador de terminación, la ejecución debería continuar hasta el final del bloque.</span><span class="sxs-lookup"><span data-stu-id="3a8df-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="3a8df-127">También puede ejecutar la instrucción **\_ \_ leave** .</span><span class="sxs-lookup"><span data-stu-id="3a8df-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="3a8df-128">La instrucción **\_ \_ leave** permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3a8df-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="3a8df-129">Consulte la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave** .</span><span class="sxs-lookup"><span data-stu-id="3a8df-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="3a8df-130">Si finaliza la ejecución del bloque **\_ \_ Finally** debido a la instrucción de control **devuelto** , es equivalente a un **goto** a la llave de cierre de la función de inclusión.</span><span class="sxs-lookup"><span data-stu-id="3a8df-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="3a8df-131">Por lo tanto, la función de inclusión devolverá.</span><span class="sxs-lookup"><span data-stu-id="3a8df-131">Therefore, the enclosing function will return.</span></span>

 

 
