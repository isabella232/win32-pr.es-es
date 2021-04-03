---
title: Indicar errores por excepciones
description: En el caso de los programadores de C tradicionales, los errores se devuelven normalmente a través de los valores devueltos o un parámetro especial \ out \ que devuelve el código de error.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904724"
---
# <a name="indicate-errors-by-exceptions"></a>Indicar errores por excepciones

En el caso de los programadores de C tradicionales, los errores se devuelven normalmente a través de los valores devueltos o un \[ parámetro out especial \] que devuelve el código de error. Esto conduce a las interfaces implementadas de la siguiente manera:

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

El problema con este enfoque es que los valores devueltos de RPC son simplemente enteros largos. No tienen ningún significado especial como errores (tenga en cuenta que el [**Estado de error \_ \_ t**](/windows/desktop/Midl/error-status-t) no tiene ninguna semántica especial en el lado servidor), lo que conlleva importantes implicaciones.

En primer lugar, RPC no se avisa de que se produjo un error en la operación. intenta anular las referencias de todos los \[ argumentos in, out \] y \[ out \] . La semántica de errores de los identificadores de contexto también es diferente. El paquete devuelto al cliente es esencialmente un paquete correcto, con el código de error escondido en el paquete. Esto también significa que RPC no utiliza la información de error extendida, por lo que el software cliente a menudo no puede discernir dónde se produjo un error en la llamada.

Indicar errores en las rutinas de servidor RPC mediante la generación de excepciones de control de excepciones estructurado (SEH) (no C++) es un enfoque mucho mejor. Cuando se inicia una excepción SEH, el control pasa directamente a la hora de ejecución de RPC. A veces se produce un error en una rutina que no se puede limpiar correctamente y debe indicar un error a su llamador. La rutina debe devolver un error a su llamador, que a su vez puede devolver un error al autor de la llamada, etc. Sin embargo, la última rutina de servidor en la pila debe iniciar una excepción antes de que vuelva a RPC para indicar a RPC que se ha producido un error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de excepciones](exception-handling.md)
</dt> </dl>

 

 