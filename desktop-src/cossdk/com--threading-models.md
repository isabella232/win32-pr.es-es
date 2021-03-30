---
description: Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento. Un contenedor es una colección de contextos contenidos en un proceso.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de subprocesos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "103819842"
---
# <a name="com-threading-models"></a>Modelos de subprocesos COM+

Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento. Un contenedor es una colección de contextos contenidos en un proceso, tal como se muestra en la siguiente ilustración.

![Diagrama que muestra una colección de contextos en una actividad, dentro de un apartamento, dentro de un proceso.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Las llamadas dentro de un contenedor son directas, mientras que las llamadas entre apartamentos (fuera de proceso) son indirectas y requieren código de proxy y código auxiliar. Los apartamentos permiten objetos con diferentes propiedades de sincronización y reentrada y tienen dos categorías: de un solo subproceso y multiproceso. Los objetos de un contenedor uniproceso (STA) se ejecutan en el subproceso determinado en el que se crearon. Sta permite que solo se ejecute un método a la vez. Están diseñados para las interfaces de usuario y se basan en la cola de mensajes de Microsoft Windows para procesar las llamadas entrantes.

Los objetos de un contenedor multiproceso (MTA) se ejecutan en cualquier subproceso y permiten que se produzca cualquier número de métodos simultáneamente. Los MTA admiten la reentrada implícitamente.

Las clases COM+ se marcan con una propiedad **ThreadingModel** que permite a com+ crear el objeto en el apartamento adecuado. Para determinar en qué apartamento se crea un objeto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa la propiedad **ThreadingModel** .

Los subprocesos deben llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para poder usar com+. Esto los crea dentro del apartamento y el contexto correctos. Se determina que el apartamento del subproceso principal es el primer STA llamado por **CoInitializeEx**. Normalmente se asocia con el subproceso principal de un proceso. **CoInitializeEx** indica el tipo de Apartamento requerido por el subproceso mediante el establecimiento de las marcas siguientes:

-   **COinit \_ Multithreaded**: localiza el subproceso en el apartamento multiproceso único.
-   **COinit \_ APARTMENTTHREADED**: coloca el subproceso en un nuevo STA.

En los siguientes temas de esta sección se proporciona más información acerca del uso de los modelos de subprocesos y apartamentos en COM+:

-   [Atributo del modelo de subprocesos](threading-model-attribute.md)
-   [Apartamentos neutros](neutral-apartments.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesos, subprocesos y apartamentos](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
