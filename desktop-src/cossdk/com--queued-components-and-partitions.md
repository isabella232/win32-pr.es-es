---
description: El servicio de componentes en cola COM+ es totalmente compatible con el concepto de particiones. Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente se ejecuta finalmente dentro de la partición de componentes.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Particiones y componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538614"
---
# <a name="com-queued-components-and-partitions"></a>Particiones y componentes en cola de COM+

El servicio de componentes en cola COM+ es totalmente compatible con el concepto de particiones. Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente se ejecuta finalmente dentro de la partición del componente.

## <a name="queue-names-for-partitioned-components"></a>Nombres de cola para componentes con particiones

Tradicionalmente, el servicio de componentes en cola utiliza el nombre de la aplicación como el nombre de la cola. Esto significa que en un escenario sin particiones, donde solo existe una instancia de un nombre de aplicación en un equipo, cada nombre de aplicación tiene su propia cola de mensajes.

Sin embargo, en el caso de las particiones, donde pueden existir varias instancias del mismo nombre de aplicación en un equipo, el servicio de componentes en cola utiliza la misma cola para todos los componentes en cola que comparten el mismo nombre de aplicación.

## <a name="activating-queued-components"></a>Activar componentes en cola

Las mismas reglas sobre cómo se usa el identificador de partición para activar un componente que no está en cola se aplican a un componente en cola, como se indica a continuación:

-   Si se usa un moniker para activar el componente en cola y se incluye un identificador de partición, se utiliza este ID. de partición para ubicar la partición. Este identificador de partición tiene prioridad sobre cualquier ID. de partición que pueda existir en el contexto del componente que se está activando.
-   Si no se usa ningún moniker para activar el componente, se usa el ID. de partición que se encuentra en el contexto del objeto.
-   Si no existe ningún ID. de partición en el contexto del objeto, se usa la asignación de usuario a partición predeterminada dentro de Active Directory.

> [!Note]  
> Si un equipo servidor está desconectado de la red y se cambia la asignación de usuario a partición del conjunto mientras el servidor está desconectado, es posible que la memoria caché de particiones contenga una asignación de conjunto de usuario a partición no actualizada. Esto podría dar lugar a un error de activación si la asignación de un usuario a un conjunto de particiones es el mecanismo usado para activar un componente.

 

Los eventos COM+ están totalmente integrados en las particiones. Esto significa que un suscriptor puede suscribirse a un publicador cuya aplicación reside en una partición. Para permitir esta suscripción, la colección de clases de suscriptores incluye dos propiedades relacionadas con la partición: un identificador de partición de clase de evento y un identificador de aplicación de clase de evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



