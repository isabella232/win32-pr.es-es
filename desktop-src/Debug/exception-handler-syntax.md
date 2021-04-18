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
# <a name="exception-handler-syntax"></a>Sintaxis de Exception-Handler

Las palabras clave **\_ \_ try** y **\_ \_ Except** se usan para construir un controlador de excepciones basado en marcos. En el ejemplo siguiente se muestra la estructura de un controlador de excepciones.


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



Tenga en cuenta que el bloque **\_ \_ try** y el bloque de controlador de excepciones requieren llaves ( {} ). No se permite usar una instrucción **goto** para saltar al cuerpo de un bloque **\_ \_ try** o a un bloque de controlador de excepciones. Esta regla se aplica tanto a los controladores de excepciones como a los controladores de terminación.

El bloque **\_ \_ try** contiene el cuerpo protegido del código que el controlador de excepciones protege. Una función puede tener cualquier número de controladores de excepciones, y estas instrucciones de control de excepciones se pueden anidar dentro de la misma función o en funciones diferentes. Si se produce una excepción dentro del bloque **\_ \_ try** , el sistema toma el control y comienza la búsqueda de un controlador de excepciones. Para obtener una descripción detallada de esta búsqueda, consulte [control de excepciones](exception-handling.md).

El controlador de excepciones recibe solo las excepciones que se producen dentro de un único subproceso. Esto significa que si un bloque **\_ \_ try** contiene una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , las excepciones que se producen dentro del proceso o subproceso nuevo no se envían a este controlador.

El sistema evalúa la expresión de filtro de cada controlador de excepciones que protege el código en el que se produjo la excepción hasta que se controla la excepción o no hay más controladores. Una expresión de filtro debe evaluarse como uno de los tres valores siguientes.



| Value                              | Significado                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_controlador de ejecución de excepción \_**    | El sistema transfiere el control al controlador de excepciones y la ejecución continúa en el marco de pila en el que se encuentra el controlador.                                                                                       |
| **EXCEPTION \_ continue \_ Search**    | El sistema continúa buscando un controlador.                                                                                                                                                                          |
| **ejecución de excepción \_ continua \_** | El sistema detiene su búsqueda de un controlador y devuelve el control al punto en el que se produjo la excepción. Si la excepción no es continuable, se produce una excepción de excepción no **\_ \_ continuada de excepción** . |



 

La expresión de filtro se evalúa en el contexto de la función en la que se encuentra el controlador de excepciones, aunque la excepción puede haberse producido en una función diferente. Esto significa que la expresión de filtro puede tener acceso a las variables locales de la función. Del mismo modo, el bloque de controlador de excepciones puede tener acceso a las variables locales de la función en la que se encuentra.

Para obtener más ejemplos, vea [usar un controlador de excepciones](using-an-exception-handler.md).

Para obtener más información sobre las expresiones de filtro y las funciones de filtro, vea [control de excepciones basado en marcos](frame-based-exception-handling.md).

 

 
