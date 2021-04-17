---
description: En los siguientes ejemplos se muestra el uso de un controlador de excepciones.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Usar un controlador de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659552"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="8662d-103">Usar un controlador de excepciones</span><span class="sxs-lookup"><span data-stu-id="8662d-103">Using an Exception Handler</span></span>

<span data-ttu-id="8662d-104">En los siguientes ejemplos se muestra el uso de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="8662d-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="8662d-105">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8662d-105">Example 1</span></span>

<span data-ttu-id="8662d-106">En el fragmento de código siguiente se usa el control de excepciones estructurado para comprobar si una operación de división en enteros de 2 32 bits producirá un error de división por cero.</span><span class="sxs-lookup"><span data-stu-id="8662d-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="8662d-107">Si esto ocurre, la función devuelve **false**; de lo contrario, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="8662d-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="8662d-108">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="8662d-108">Example 2</span></span>

<span data-ttu-id="8662d-109">La función de ejemplo siguiente llama a la función [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) y usa el control de excepciones estructurado para comprobar si hay una excepción de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8662d-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="8662d-110">Si se produce una, la función devuelve **false**; de lo contrario, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="8662d-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="8662d-111">La expresión de filtro en el ejemplo usa la función [**GetExceptionCode**](getexceptioncode.md) para comprobar el tipo de excepción antes de ejecutar el controlador.</span><span class="sxs-lookup"><span data-stu-id="8662d-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="8662d-112">Esto permite que el sistema siga buscando un controlador adecuado si se produce algún otro tipo de excepción.</span><span class="sxs-lookup"><span data-stu-id="8662d-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="8662d-113">Además, el uso de la instrucción **Return** en el bloque **\_ \_ try** de un controlador de excepciones difiere del uso de **Return** en el bloque **\_ \_ try** de un controlador de finalización, lo que produce una terminación anómala del bloque **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="8662d-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="8662d-114">Se trata de un uso válido de la instrucción return en un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="8662d-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="8662d-115">Devuelva solo \_ \_ el controlador de ejecución de excepciones desde un filtro de excepción cuando se espera el tipo de excepción y se conoce la dirección de error.</span><span class="sxs-lookup"><span data-stu-id="8662d-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="8662d-116">Debe permitir que el controlador de excepciones predeterminado procese tipos de excepción inesperados y direcciones erróneas.</span><span class="sxs-lookup"><span data-stu-id="8662d-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="8662d-117">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="8662d-117">Example 3</span></span>

<span data-ttu-id="8662d-118">En el ejemplo siguiente se muestra la interacción de los controladores anidados.</span><span class="sxs-lookup"><span data-stu-id="8662d-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="8662d-119">La función [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) produce una excepción en el cuerpo protegido de un controlador de terminación que se encuentra dentro del cuerpo protegido de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="8662d-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="8662d-120">La excepción hace que el sistema evalúe la función FilterFunction, cuyo valor devuelto a su vez hace que se invoque el controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="8662d-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="8662d-121">Sin embargo, antes de que se ejecute el bloque de controlador de excepciones, el bloque **\_ \_ Finally** del controlador de terminación se ejecuta porque el flujo de control ha dejado el bloque **\_ \_ try** del controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="8662d-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
