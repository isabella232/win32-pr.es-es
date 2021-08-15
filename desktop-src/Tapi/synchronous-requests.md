---
description: Los diseñadores de proveedores de servicios deben intentar mantener corto el tiempo de ejecución de las operaciones sincrónicas.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Solicitudes sincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e399fcef1ffba574305b70aee05d7430bcd84746458198b3d33ed6bb0848747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760707"
---
# <a name="synchronous-requests"></a>Solicitudes sincrónicas

Los diseñadores de proveedores de servicios deben intentar mantener corto el tiempo de ejecución de las operaciones sincrónicas. Por ejemplo, hay una operación "Open" llamada en el momento de la inicialización que prepara el proveedor de servicios y TAPI para las operaciones posteriores en un dispositivo. Un proveedor de servicios cuya implementación se divide entre el equipo cliente y un servidor dedicado puede tener una confianza razonable de que puede comunicarse con su servidor remoto. Su implementación de "Open" podría simplemente asignar e inicializar estructuras de datos para representar el dispositivo y devolver, posponiendo la comunicación de un extremo a otro hasta que se solicite alguna operación real.

Cualquier implementación "optimista" de una operación sincrónica puede encontrar más adelante limitaciones de recursos o errores de comunicación remota. En general, incluso un enfoque "conservador" no puede evitar completamente estos problemas. los diseñadores de proveedores de servicios deben elegir el mejor equilibrio entre la confiabilidad y el rendimiento. Un error de este tipo debe controlarse correctamente siempre que sea posible. Desde el punto de vista de los dispositivos TSPI, deben seguir siendo válidos con fines de "contabilidad", incluso si devuelven el estado de error para cualquier operación solicitada.

La implementación de un enfoque optimista para las solicitudes sincrónicas no debe realizarse a costa de la semántica correcta para la operación. Volviendo al ejemplo "Abierto", si la apertura de un dispositivo necesita competir y reservar un recurso insuficiente y no compartido, como los puertos de comunicación, probablemente debería hacerlo incluso si lleva mucho tiempo.

**TAPI 2.x:** Una operación que se completa sincrónicamente realiza todo su procesamiento en la llamada de función realizada por la aplicación. La función devuelve valores diferentes en función de su éxito o error:

-   **Sincrónica correcta.** Si la solicitud o el servicio correspondiente a la función se ha realizado correctamente, la función devuelve cero, lo que indica que se ha realizado correctamente. Los valores escritos como resultado de la llamada de función son confiables y se pueden usar inmediatamente.
-   **Error sincrónico.** Si la función detecta un error y no se lleva a cabo la solicitud, se devuelve un número de error negativo para identificar el error.

 

 



