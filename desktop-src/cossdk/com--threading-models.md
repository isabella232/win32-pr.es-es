---
description: Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento. Un apartamento es una colección de contextos contenidos en un proceso.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de subprocesamiento de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0949a27291be43b5981f24f4985fac6911937b2c9fa85785b4d662bd1bf546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793685"
---
# <a name="com-threading-models"></a>Modelos de subprocesamiento de COM+

Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento. Un apartamento es una colección de contextos contenidos en un proceso, como se muestra en la ilustración siguiente.

![Diagrama que muestra una colección de contextos en una actividad, dentro de un apartamento, dentro de un proceso.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Las llamadas dentro de un apartamento son directas, mientras que las llamadas entre departamentos (fuera de proceso) son indirectas y requieren código proxy y stub. Los departamentos permiten objetos con diferentes propiedades de sincronización y reenlazancia y tienen dos categorías: de subproceso único y multiproceso. Los objetos de un solo subproceso (STA) se ejecutan en el subproceso concreto en el que se crearon. Las STA solo permiten que un método se ejecute a la vez. Están diseñados para interfaces de usuario y se basan en microsoft Windows cola de mensajes para procesar las llamadas entrantes.

Los objetos de un apartamento multiproceso (MTA) se ejecutan en cualquier subproceso y permiten que cualquier número de métodos se produzca simultáneamente. Los MTA admiten la reenvía implícitamente.

Las clases COM+ se marcan con **una propiedad ThreadingModel** que permite a COM+ crear el objeto en el apartamento adecuado. Para determinar en qué apartamento se crea un objeto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa la **propiedad ThreadingModel.**

Los subprocesos deben [**llamar a CoInitializeEx para**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) poder usar COM+. Esto los crea dentro del apartamento y el contexto correctos. El apartamento del subproceso principal se determina como el primer STA llamado por **CoInitializeEx**. Esto suele estar asociado al subproceso principal de un proceso. **CoInitializeEx** indica el tipo de apartamento requerido por el subproceso estableciendo las marcas siguientes:

-   **COINIT \_ MULTITHREADED:** busca el subproceso en el único apartamento multiproceso.
-   **COINIT \_ APARTMENTTHREADED:** coloca el subproceso en un nuevo STA.

Los temas siguientes de esta sección proporcionan más información sobre el uso de modelos de subprocesos y departamentos en COM+:

-   [Atributo del modelo de subprocesos](threading-model-attribute.md)
-   [NeutralEstes](neutral-apartments.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesos, subprocesos y departamentos](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
