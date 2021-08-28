---
description: Las \_ \_ palabras clave try y except se \_ \_ usan para construir un controlador de excepciones basado en fotogramas. En el ejemplo siguiente se muestra la estructura de un controlador de excepciones.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd24b3ffc84a3469c7c8d97ce505a0292ee538ea8f0b9c1d604bf34f65203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912745"
---
# <a name="exception-handler-syntax"></a>Exception-Handler sintaxis

Las **\_ \_ palabras clave try** y **\_ \_ except** se usan para construir un controlador de excepciones basado en fotogramas. En el ejemplo siguiente se muestra la estructura de un controlador de excepciones.


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



Tenga en cuenta que **\_ \_ el bloque try** y el bloque de controlador de excepciones requieren llaves ( {} ). No se **permite usar una instrucción goto** para saltar al cuerpo de un bloque **\_ \_ try** o a un bloque de controlador de excepciones. Esta regla se aplica tanto a los controladores de excepciones como a los controladores de terminación.

El **\_ \_ bloque try** contiene el cuerpo de código guardado que protege el controlador de excepciones. Una función puede tener cualquier número de controladores de excepciones y estas instrucciones de control de excepciones se pueden anidar dentro de la misma función o en funciones diferentes. Si se produce una excepción dentro del **\_ \_ bloque try,** el sistema toma el control y comienza la búsqueda de un controlador de excepciones. Para obtener una descripción detallada de esta búsqueda, vea [Control de excepciones.](exception-handling.md)

El controlador de excepciones recibe solo las excepciones que se producen dentro de un único subproceso. Esto significa que si un bloque **\_ \_ try** contiene una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) las excepciones que se producen dentro del nuevo proceso o subproceso no se envían a este controlador.

El sistema evalúa la expresión de filtro de cada controlador de excepciones que protege el código en el que se produjo la excepción hasta que se controla la excepción o no hay más controladores. Una expresión de filtro debe evaluarse como uno de los tres valores siguientes.



| Value                              | Significado                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EXCEPTION \_ EXECUTE \_ HANDLER**    | El sistema transfiere el control al controlador de excepciones y la ejecución continúa en el marco de pila en el que se encuentra el controlador.                                                                                       |
| **EXCEPTION \_ CONTINUE \_ SEARCH**    | El sistema continúa buscando un controlador.                                                                                                                                                                          |
| **EXCEPTION \_ CONTINUE \_ EXECUTION** | El sistema detiene la búsqueda de un controlador y devuelve el control al punto en el que se produjo la excepción. Si la excepción no es pertinente, se produce una excepción **EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION.** |



 

La expresión de filtro se evalúa en el contexto de la función en la que se encuentra el controlador de excepciones, aunque la excepción se haya producido en una función diferente. Esto significa que la expresión de filtro puede tener acceso a las variables locales de la función. De forma similar, el bloque de controlador de excepciones puede tener acceso a las variables locales de la función en la que se encuentra.

Para obtener más ejemplos, [vea Usar un controlador de excepciones.](using-an-exception-handler.md)

Para obtener más información sobre las expresiones de filtro y las funciones de filtro, vea [Control de excepciones basado en fotogramas.](frame-based-exception-handling.md)

 

 
