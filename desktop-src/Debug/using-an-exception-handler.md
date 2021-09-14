---
description: En los ejemplos siguientes se muestra el uso de un controlador de excepciones.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Usar un controlador de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164557"
---
# <a name="using-an-exception-handler"></a>Usar un controlador de excepciones

En los ejemplos siguientes se muestra el uso de un controlador de excepciones.

## <a name="example-1"></a>Ejemplo 1

El fragmento de código siguiente usa el control estructurado de excepciones para comprobar si una operación de división en dos enteros de 32 bits producirá un error de división por cero. Si esto ocurre, la función devuelve **FALSE;** de lo contrario, **devuelve TRUE.**


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



## <a name="example-2"></a>Ejemplo 2

La siguiente función de ejemplo llama a la [**función DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) y usa el control de excepciones estructurado para comprobar si hay una excepción de punto de interrupción. Si se produce una, la función devuelve **FALSE;** de lo contrario, **devuelve TRUE**.

La expresión de filtro del ejemplo usa la [**función GetExceptionCode**](getexceptioncode.md) para comprobar el tipo de excepción antes de ejecutar el controlador. Esto permite al sistema continuar con la búsqueda de un controlador adecuado si se produce algún otro tipo de excepción.

Además, el uso de la instrucción **return** en el bloque **\_ \_ try** de un controlador de excepciones difiere del uso de **return** en el bloque **\_ \_ try** de un controlador de terminación, lo que provoca una terminación anómala del **\_ \_ bloque try.** Se trata de un uso válido de la instrucción return en un controlador de excepciones.


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



Solo se devuelve EXCEPTION EXECUTE HANDLER desde un filtro de excepción cuando se espera el tipo de excepción \_ y se conoce la dirección de \_ error. Debe permitir que el controlador de excepciones predeterminado procese tipos de excepción inesperados y direcciones con errores.

## <a name="example-3"></a>Ejemplo 3

En el ejemplo siguiente se muestra la interacción de los controladores anidados. La [**función RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) produce una excepción en el cuerpo guardado de un controlador de terminación que está dentro del cuerpo de protección de un controlador de excepciones. La excepción hace que el sistema evalúe la función FilterFunction, cuyo valor devuelto a su vez hace que se invoque el controlador de excepciones. Sin embargo, antes de ejecutar el bloque de controlador de excepciones, se ejecuta el bloque **\_ \_ finally** del controlador de terminación porque el flujo de control ha dejado el bloque **\_ \_ try** del controlador de terminación.


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



 

 
