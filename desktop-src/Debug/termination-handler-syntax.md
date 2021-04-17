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
# <a name="termination-handler-syntax"></a>Sintaxis de Termination-Handler

Las palabras clave **\_ \_ try** y **\_ \_ Finally** se usan para construir un controlador de finalización. En el ejemplo siguiente se muestra la estructura de un controlador de terminación.


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



Para obtener ejemplos, vea [usar un controlador de terminación](using-a-termination-handler.md).

Al igual que con el controlador de excepciones, tanto el bloque **\_ \_ try** como el bloque **\_ \_ Finally** requieren llaves ( {} ), y no se permite el uso de una instrucción **goto** para saltar a cualquiera de los bloques.

El bloque **\_ \_ try** contiene el cuerpo protegido del código que está protegido por el controlador de terminación. Una función puede tener cualquier número de controladores de terminación y estos bloques de control de terminación se pueden anidar dentro de la misma función o en funciones diferentes.

El bloque **\_ \_ Finally** se ejecuta siempre que el flujo de control sale del bloque **\_ \_ try** . Sin embargo, el bloque **\_ \_ Finally** no se ejecuta si se llama a cualquiera de las siguientes funciones en el bloque **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **Abort**.

El bloque **\_ \_ Finally** se ejecuta en el contexto de la función en la que se encuentra el controlador de terminación. Esto significa que el bloque **\_ \_ Finally** puede tener acceso a las variables locales de la función. La ejecución del bloque **\_ \_ Finally** puede finalizar con cualquiera de los siguientes medios.

-   Ejecución de la última instrucción en el bloque y continuación a la siguiente instrucción
-   Uso de una instrucción de control (**Return**, **break**, **continue** o **goto**)
-   Uso de **longjmp** o un salto a un controlador de excepciones

Si la ejecución del bloque **\_ \_ try** finaliza debido a una excepción que invoca el bloque de control de excepciones de un controlador de excepciones basado en marcos, el bloque **\_ \_ Finally** se ejecuta antes de que se ejecute el bloque de control de excepciones. Del mismo modo, una llamada a la función de biblioteca en tiempo de ejecución de C de **longjmp** desde el bloque **\_ \_ try** produce la ejecución del bloque **\_ \_ Finally** antes de que se reanude la ejecución en el destino de la operación **longjmp** . Si la ejecución de bloque **\_ \_ try** finaliza debido a una instrucción de control (**Return**, **break**, **continue** o **goto**), se ejecuta el bloque **\_ \_ Finally** .

La función [**AbnormalTermination**](abnormaltermination.md) se puede usar en el bloque **\_ \_ Finally** para determinar si el bloque **\_ \_ try** terminó secuencialmente, es decir, si llegó a la llave de cierre (}). Si se deja el bloque **\_ \_ try** debido a una llamada a **longjmp**, un salto a un controlador de excepciones o una instrucción **Return**, **break**, **continue** o **goto** , se considera una terminación anómala. Tenga en cuenta que si no se termina secuencialmente, el sistema busca en todos los marcos de pila en orden inverso para determinar si se debe llamar a algún controlador de finalización. Esto puede producir una degradación del rendimiento debido a la ejecución de cientos de instrucciones.

Para evitar la terminación anómala del controlador de terminación, la ejecución debería continuar hasta el final del bloque. También puede ejecutar la instrucción **\_ \_ leave** . La instrucción **\_ \_ leave** permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento. Consulte la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave** .

Si finaliza la ejecución del bloque **\_ \_ Finally** debido a la instrucción de control **devuelto** , es equivalente a un **goto** a la llave de cierre de la función de inclusión. Por lo tanto, la función de inclusión devolverá.

 

 
