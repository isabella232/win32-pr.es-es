---
description: Conceptos de eventos COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Conceptos de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807964"
---
# <a name="com-events-concepts"></a>Conceptos de eventos COM+

El servicio de eventos COM+ es un sistema de eventos automatizado y de *acoplamiento flexible* que almacena información de eventos de distintos publicadores en el catálogo de com+. Los suscriptores pueden consultar este almacén de eventos y seleccionar los eventos sobre los que desean conocer.

> [!Note]  
> Un *evento* se identifica mediante un método en una interfaz com+, conocido como *método de evento*, y se origina en un publicador y se envía al suscriptor o suscriptores correctos mediante el servicio de eventos com+. Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada (sin parámetros de salida o de entrada/salida). El valor devuelto debe ser **HRESULT**.

 

El servicio de eventos COM+ controla la mayor parte de la semántica de eventos para el publicador y el suscriptor. Los publicadores ofrecen para publicar tipos de eventos y los suscriptores solicitan tipos de eventos de los publicadores. A diferencia de un sistema de *eventos estrechamente acoplado* , en el que los publicadores deben controlar la sobrecarga de llamar directamente a los suscriptores, el servicio de eventos com+ mantiene los datos de suscripción en el catálogo de com+, independientemente del publicador y del suscriptor. Esto simplifica el modelo de programación para el publicador y el suscriptor porque el componente de suscriptor de COM+ no necesita contener la lógica para la creación de suscripciones.

Dado que el ciclo de vida de los datos de suscripciones de eventos COM+ es independiente del publicador o del suscriptor, las suscripciones se pueden crear antes de que las aplicaciones del suscriptor o del publicador estén activas. Esto también significa que los publicadores y suscriptores se pueden desarrollar e implementar por separado. El publicador se puede escribir sin conocimiento del número y la ubicación de los suscriptores. Los suscriptores usan el servicio de eventos COM+ para buscar el publicador y administrar sus suscripciones.

En los siguientes temas de esta sección se proporciona información detallada sobre los elementos básicos del servicio de eventos COM+ y cómo usarlos.

-   [Objeto de la clase de eventos COM+](the-com--event-class-object.md)
-   [Suscripciones](subscriptions.md)
-   [Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
-   [Filtrado de eventos en COM+](filtering-events-in-com-.md)
-   [Usar eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Tareas de eventos COM+](com--events-tasks.md)
</dt> </dl>

 

 



