---
description: El servicio de componentes en cola de COM+ admite totalmente el concepto de particiones. Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente finalmente se ejecuta dentro de la partición de componentes.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componentes y particiones en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0296119d32eafefd3212ae37e32543b8fd14b884ff6401c16827717a9a6960b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129077"
---
# <a name="com-queued-components-and-partitions"></a>Componentes y particiones en cola de COM+

El servicio de componentes en cola de COM+ admite totalmente el concepto de particiones. Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente finalmente se ejecuta dentro de la partición del componente.

## <a name="queue-names-for-partitioned-components"></a>Nombres de cola para componentes con particiones

Tradicionalmente, el servicio de componentes en cola usa el nombre de la aplicación como nombre de cola. Esto significa que en un escenario sin particiones, donde solo existe una instancia de un nombre de aplicación en un equipo, cada nombre de aplicación tiene su propia cola de mensajes.

Sin embargo, en el caso de las particiones en las que pueden existir varias instancias del mismo nombre de aplicación en un equipo, el servicio de componentes en cola usa la misma cola para los componentes en cola que comparten el mismo nombre de aplicación.

## <a name="activating-queued-components"></a>Activación de componentes en cola

Las mismas reglas para usar el identificador de partición para activar un componente no en cola se aplican a un componente en cola, como se muestra a continuación:

-   Si se usa un moniker para activar el componente en cola y se incluye un identificador de partición, este identificador de partición se usa para buscar la partición. Este identificador de partición tiene prioridad sobre cualquier identificador de partición que pueda existir en el contexto del componente que se está activando.
-   Si no se usa ningún moniker para activar el componente, se usa el identificador de partición que se encuentra en el contexto del objeto.
-   Si no existe ningún identificador de partición en el contexto del objeto, se usa la asignación de usuario a partición predeterminada Active Directory.

> [!Note]  
> Si un equipo servidor está desconectado de la red y la asignación del conjunto de usuarios a particiones cambia mientras el servidor está desconectado, la caché de particiones podría contener una asignación de conjunto de usuario a partición obsoleta. Esto podría producir un error de activación si la asignación de conjunto de usuario a partición es el mecanismo utilizado para activar un componente.

 

Los eventos COM+ están totalmente integrados en particiones. Esto significa que un suscriptor puede suscribirse a un publicador cuya aplicación reside dentro de una partición. Para permitir esta suscripción, la colección de clases de suscriptor incluye dos propiedades relacionadas con la partición: un identificador de partición de clase de eventos y un identificador de aplicación de clase de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Implementación de partición](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



