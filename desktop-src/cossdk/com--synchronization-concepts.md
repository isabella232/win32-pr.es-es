---
description: Por lo general, la sincronización no es necesaria cuando se tiene un apartamento de un solo subproceso (STA) porque el apartamento proporciona la sincronización automáticamente.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceptos de sincronización de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258559"
---
# <a name="com-synchronization-concepts"></a>Conceptos de sincronización de COM+

Por lo general, la sincronización no es necesaria cuando se tiene un apartamento de un solo subproceso (STA) porque el apartamento proporciona la sincronización automáticamente. La sincronización es importante cuando tiene un apartamento multiproceso (MTA) y un objeto de subproceso libre. En el pasado, los objetos de subproceso libre tenían que controlar el bloqueo. Puede eliminar la necesidad de usar el bloqueo estableciendo el atributo de sincronización para un componente.

La sincronización tiene las siguientes propiedades:

-   Permite que un llamador escriba el componente a la vez.
-   Prohíbe el flujo entre procesos o equipos.
-   Fluye de componente a componente dentro de un proceso.
-   Permite la reenlazancia del mismo autor de la llamada.

A diferencia de los departamentos, las actividades abarcan contextos de varios procesos y hosts. La sincronización determina qué actividad contendrá un objeto . Los objetos pueden residir en cualquiera de las actividades siguientes:

-   Actividad del creador
-   Nueva actividad
-   Sin actividad

COM+ garantiza la simultaneidad mediante una serie de bloqueos para cada actividad. Si un autor de la llamada intenta escribir un componente sincronizado de COM+ que ya está siendo utilizado por otro llamador, la llamada se bloquea hasta que se libera el bloqueo. Este comportamiento de bloqueo no dará tiempo de espera y no se puede configurar para que se resalte el tiempo de espera. Si el bloqueo no está en uso, se adquiere el bloqueo y se procesa la llamada. Después de completarse, se libera el bloqueo para el siguiente llamador. Para evitar interbloqueos, COM+ administra el acceso a todos los objetos de las actividades mediante una serie anidada de llamadas encadenadas en toda la red.

COM+ proporciona la siguiente configuración de sincronización:

-   Disabled
-   No compatible
-   Compatible
-   Obligatorio
-   Se requiere nueva

> [!Note]  
> Algunas configuraciones de sincronización funcionan junto con otras configuraciones de componentes com+. Por ejemplo, la sincronización es necesaria si el servicio de activación [Just-In-Time (JIT)](com--just-in-time-activation.md) de COM+ está habilitado. JIT es necesario si habilita las transacciones; por lo tanto, el procesamiento [de transacciones COM+](com--transactions.md) también requiere sincronización. Por lo tanto, las clases con el valor JIT=True también deben tener el valor Synchronization=Required o Synchronization=RequiresNew.

 

Para obtener instrucciones sobre cómo establecer las opciones de sincronización mediante la herramienta administrativa Servicios de componentes, vea [Establecer el atributo de sincronización](setting-the-synchronization-attribute.md).

Para obtener más información sobre el uso de la biblioteca de administración de COM+ para establecer opciones de sincronización, vea [Automatización de la administración de COM+.](automating-com--administration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de sincronización de COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



