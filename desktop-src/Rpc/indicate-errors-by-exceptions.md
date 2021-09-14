---
title: Indicar errores por excepciones
description: Para los programadores de C tradicionales, los errores se devuelven normalmente a través de valores devueltos o un parámetro especial \out\ que devuelve el código de error.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244616"
---
# <a name="indicate-errors-by-exceptions"></a>Indicar errores por excepciones

Para los programadores de C tradicionales, los errores se devuelven normalmente a través de valores devueltos o un parámetro de salida especial \[ que devuelve el código de \] error. Esto conduce a interfaces implementadas de la siguiente manera:

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

El problema con este enfoque es que los valores devueltos de RPC son simplemente enteros largos. No tienen ningún significado especial como errores (tenga en cuenta que el estado de [**error \_ \_ t**](/windows/desktop/Midl/error-status-t) no tiene ninguna semántica especial en el lado servidor), lo que conlleva implicaciones importantes.

En primer lugar, no se alerta a RPC de que se ha podido hacer la operación; intenta desmarshal todos los argumentos \[ de entrada, \] salida y \[ \] salida. La semántica de error de los identificadores de contexto también es diferente. El paquete devuelto al cliente es básicamente un paquete correcto, con el código de error en la profundidad del paquete. Esto también significa que RPC no usa información de error extendida, por lo que el software cliente a menudo no puede distinguir dónde se produjo un error en la llamada.

Indicar errores en las rutinas de servidor RPC mediante el lanzamiento de excepciones de Control de excepciones estructurado (SEH) (no C++) es un enfoque mucho mejor. Cuando se produce una excepción SEH, el control pasa directamente al tiempo de ejecución de RPC. A veces, un error se produce en una rutina que no se puede limpiar correctamente y debe indicar un error a su autor de la llamada. La rutina debe devolver un error a su llamador, que a su vez puede devolver un error a su autor de la llamada, y así sucesivamente. Sin embargo, la última rutina de servidor de la pila debe producir una excepción antes de volver a RPC para indicar a RPC que se ha producido un error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de excepciones](exception-handling.md)
</dt> </dl>

 

 