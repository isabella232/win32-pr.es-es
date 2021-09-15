---
description: Conceptos de eventos COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Conceptos de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476108"
---
# <a name="com-events-concepts"></a>Conceptos de eventos COM+

El servicio de eventos COM+ es un sistema de eventos automatizado y de acoplamiento flexible que almacena información de eventos de distintos publicadores en el catálogo de COM+.  Los suscriptores pueden consultar este almacén de eventos y seleccionar los eventos que quieren conocer.

> [!Note]  
> Un  evento se identifica mediante un método en una interfaz COM+, conocido como método de evento *,* y se origina en un publicador y se envía al suscriptor o suscriptores correctos a través del servicio de eventos COM+. Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada (sin parámetros de salida o de entrada/salida). El valor devuelto debe ser **HRESULT.**

 

El servicio de eventos COM+ controla la mayor parte de la semántica de eventos para el publicador y el suscriptor. Los publicadores ofrecen para publicar tipos de eventos y los suscriptores solicitan tipos de eventos a los publicadores. A diferencia de un sistema de eventos estrechamente acoplado, donde los publicadores deben controlar la sobrecarga de llamar *directamente* a los suscriptores, el servicio de eventos COM+ mantiene los datos de suscripción en el catálogo de COM+, independientemente del publicador y el suscriptor. Esto simplifica el modelo de programación para el publicador y el suscriptor porque el componente de suscriptor COM+ no necesita contener la lógica para compilar suscripciones.

Dado que el ciclo de vida de los datos de suscripción de eventos COM+ es independiente del del publicador o del suscriptor, las suscripciones se pueden compilar antes de que el suscriptor o las aplicaciones del publicador se activen. Esto también significa que los publicadores y suscriptores se pueden desarrollar e implementar por separado. El publicador se puede escribir sin tener conocimiento del número y la ubicación de los suscriptores. Los suscriptores usan el servicio eventos COM+ para buscar el publicador y administrar sus suscripciones.

Los temas siguientes de esta sección proporcionan información detallada sobre los elementos principales del servicio de eventos COM+ y cómo usarlos.

-   [El objeto de clase de eventos COM+](the-com--event-class-object.md)
-   [Suscripciones](subscriptions.md)
-   [Publicación y entrega de eventos en COM+](publishing-and-delivering-events-in-com-.md)
-   [Filtrado de eventos en COM+](filtering-events-in-com-.md)
-   [Uso de eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Tareas de eventos COM+](com--events-tasks.md)
</dt> </dl>

 

 



