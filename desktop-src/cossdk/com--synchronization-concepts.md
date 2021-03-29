---
description: Por lo general, la sincronización no es necesaria cuando se tiene un contenedor uniproceso (STA) porque el apartamento proporciona la sincronización automáticamente.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceptos de sincronización de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807808"
---
# <a name="com-synchronization-concepts"></a>Conceptos de sincronización de COM+

Por lo general, la sincronización no es necesaria cuando se tiene un contenedor uniproceso (STA) porque el apartamento proporciona la sincronización automáticamente. La sincronización es importante cuando tiene un contenedor multiproceso (MTA) y un objeto de subproceso libre. En el pasado, los objetos de subprocesamiento libre tenían que controlar el bloqueo. Puede eliminar la necesidad de usar el bloqueo estableciendo el atributo de sincronización de un componente.

La sincronización tiene las siguientes propiedades:

-   Permite a un llamador entrar en el componente a la vez.
-   Prohíbe el flujo a través del proceso o entre equipos.
-   Fluye del componente al componente dentro de un proceso.
-   Permite la reentrada del mismo llamador.

A diferencia de apartamentos, las actividades abarcan contextos de varios procesos y hosts. La sincronización determina qué actividad contendrá un objeto. Los objetos pueden residir en cualquiera de las siguientes actividades:

-   Actividad del creador
-   Nueva actividad
-   Sin actividad

COM+ garantiza la simultaneidad mediante una serie de bloqueos para cada actividad. Si un llamador intenta entrar en un componente sincronizado de COM+ que ya está siendo utilizado por otro llamador, la llamada se bloquea hasta que se libera el bloqueo. Este comportamiento de bloqueo no agotará el tiempo de espera y no se puede configurar para que agote el tiempo de espera. Si el bloqueo no está en uso, se adquiere el bloqueo y se procesa la llamada. Después de completar, se libera el bloqueo para el siguiente autor de la llamada. Para evitar el interbloqueo, COM+ administra el acceso a todos los objetos en todas las actividades mediante una serie anidada de llamadas encadenadas a través de la red.

COM+ proporciona la siguiente configuración de sincronización:

-   Disabled
-   No compatible
-   Compatible
-   Obligatorio
-   Se requiere nueva

> [!Note]  
> Algunas configuraciones de sincronización funcionan junto con otras configuraciones de componentes de COM+. Por ejemplo, la sincronización es necesaria si está habilitado el servicio de [activación Just-in-Time (JIT) de com+](com--just-in-time-activation.md) . JIT es necesario si se habilitan las transacciones; por lo tanto, el [procesamiento de transacciones](com--transactions.md) com+ también requiere sincronización. Por lo tanto, las clases con la configuración de JIT = true también deben tener el valor de Synchronization = required o Synchronization = RequiresNew.

 

Para obtener instrucciones sobre cómo establecer las opciones de sincronización mediante la herramienta administrativa Servicios de componentes, vea [establecer el atributo de sincronización](setting-the-synchronization-attribute.md).

Para obtener más información sobre el uso de la biblioteca de administración de COM+ para establecer las opciones de sincronización, vea [automatizar la administración de com+](automating-com--administration.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de sincronización de COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



