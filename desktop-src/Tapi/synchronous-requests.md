---
description: Los diseñadores de proveedores de servicios deben intentar mantener el tiempo de ejecución de las operaciones sincrónicas en breve.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Solicitudes sincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678451"
---
# <a name="synchronous-requests"></a>Solicitudes sincrónicas

Los diseñadores de proveedores de servicios deben intentar mantener el tiempo de ejecución de las operaciones sincrónicas en breve. Por ejemplo, hay una operación "abrir" llamada en el momento de la inicialización que prepara el proveedor de servicios y TAPI para las operaciones posteriores en un dispositivo. Un proveedor de servicios cuya implementación se divida entre el equipo cliente y un servidor dedicado puede tener una confianza razonable de que puede comunicarse con su servidor remoto. Su implementación de "Open" podría simplemente asignar e inicializar las estructuras de datos para representar el dispositivo y devolver, retrasando la comunicación de un extremo a otro hasta que se solicite alguna operación real.

Cualquier implementación "optimista" de una operación sincrónica puede encontrar más adelante limitaciones de recursos o errores de comunicación remota. En general, incluso un enfoque "conservador" no puede evitar completamente estos problemas; los diseñadores de proveedores de servicios deben elegir el mejor equilibrio entre confiabilidad y rendimiento. Un error de este tipo debe controlarse correctamente siempre que sea posible. Desde el punto de vista de los dispositivos TSPI, deben seguir siendo válidos para los propósitos de "contabilidad", incluso si devuelven el estado de error para cualquier operación solicitada.

La implementación de un enfoque optimista para las solicitudes sincrónicas no se debe realizar a costa de la semántica correcta para la operación. Volviendo al ejemplo "Open", si es necesario que la apertura de un dispositivo se compitan por un recurso insuficiente y no compartible, como los puertos de comunicación, es probable que lo haga incluso si tarda mucho tiempo.

**TAPI 2. x:** Una operación que se completa de forma sincrónica realiza todo su procesamiento en la llamada de función realizada por la aplicación. La función devuelve valores diferentes en función de si se ha realizado correctamente o no:

-   **Éxito sincrónico.** Si la solicitud o servicio correspondiente a la función se ha llevado a cabo correctamente, la función devuelve cero, lo que indica que se ha realizado correctamente. Los valores escritos como resultado de la llamada de función son confiables y se pueden usar de inmediato.
-   **Error sincrónico.** Si la función detecta un error y no se realiza la solicitud, se devuelve un número de error negativo para identificar el error.

 

 



