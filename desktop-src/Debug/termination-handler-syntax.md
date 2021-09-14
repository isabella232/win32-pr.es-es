---
description: Las \_ \_ palabras clave try y finally se \_ \_ usan para construir un controlador de terminación. En el ejemplo siguiente se muestra la estructura de un controlador de terminación.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164565"
---
# <a name="termination-handler-syntax"></a>Termination-Handler sintaxis

Las **\_ \_ palabras clave try** y **\_ \_ finally** se usan para construir un controlador de terminación. En el ejemplo siguiente se muestra la estructura de un controlador de terminación.


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



Para obtener ejemplos, vea [Usar un controlador de terminación](using-a-termination-handler.md).

Al igual que con el controlador de excepciones, el bloque **\_ \_ try** y el bloque **\_ \_ finally** requieren llaves ( ) y no se permite el uso de una instrucción goto para saltar a cualquiera {} de los bloques. 

El **\_ \_ bloque try** contiene el cuerpo protegido del código protegido por el controlador de terminación. Una función puede tener cualquier número de controladores de terminación y estos bloques de control de terminación se pueden anidar dentro de la misma función o en funciones diferentes.

El **\_ \_ bloque finally** se ejecuta cada vez que el flujo de control sale del bloque **\_ \_ try.** Sin embargo, **\_ \_ el bloque finally** no se ejecuta si se llama a cualquiera de las siguientes funciones dentro del bloque **\_ \_ try:** [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **abort**.

El **\_ \_ bloque finally** se ejecuta en el contexto de la función en la que se encuentra el controlador de terminación. Esto significa que el **\_ \_ bloque finally** puede tener acceso a las variables locales de esa función. La ejecución del **\_ \_ bloque finally** puede finalizar por cualquiera de los siguientes medios.

-   Ejecución de la última instrucción en el bloque y continuación a la instrucción siguiente
-   Uso de una instrucción de control **(return**, **break**, **continue** o **goto**)
-   Uso de **longjmp o** salto a un controlador de excepciones

Si la ejecución del bloque **\_ \_ try** finaliza debido a una excepción que invoca el bloque de control de excepciones de un controlador de excepciones basado en marco, el bloque **\_ \_ finally** se ejecuta antes de que se ejecute el bloque de control de excepciones. De forma similar, una llamada a la función de biblioteca en tiempo de ejecución **de C longjmp** desde el bloque **\_ \_ try** provoca la ejecución del bloque **\_ \_ finally** antes de que se reanude la ejecución en el destino de la **operación longjmp.** Si **\_ \_ la** ejecución de bloque try finaliza debido a una instrucción de control **(devuelve**, **break**, **continue** o **goto**), **\_ \_ se** ejecuta el bloque finally.

La [**función AbnormalTermination**](abnormaltermination.md) se puede usar dentro del bloque **\_ \_ finally** para determinar si el bloque **\_ \_ try** finalizó secuencialmente, es decir, si alcanzó la llave de cierre (}). Salir del **\_ \_ bloque try** debido a una llamada a **longjmp** , un salto a un controlador de excepciones o una instrucción return , **break**, **continue** o **goto,** se considera una terminación anómala. Tenga en cuenta que el error al finalizar secuencialmente hace que el sistema busque en todos los marcos de pila en orden inverso para determinar si se debe llamar a los controladores de terminación. Esto puede provocar una degradación del rendimiento debido a la ejecución de cientos de instrucciones.

Para evitar la terminación anómala del controlador de terminación, la ejecución debe continuar hasta el final del bloque. También puede ejecutar la **\_ \_ instrucción leave.** La **\_ \_ instrucción leave** permite la terminación inmediata del bloque **\_ \_ try** sin provocar una terminación anómala y su penalización de rendimiento. Compruebe la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave.**

Si la ejecución del **\_ \_ bloque finally** finaliza debido a la instrucción de control return, es equivalente a un  **goto** a la llave de cierre de la función de cierre. Por lo tanto, la función de encier devolverá .

 

 
