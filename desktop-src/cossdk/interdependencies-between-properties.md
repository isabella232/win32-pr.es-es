---
description: Interdependencias entre propiedades
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdependencias entre propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000634"
---
# <a name="interdependencies-between-properties"></a>Interdependencias entre propiedades

Al establecer las propiedades, el catálogo de COM+ impone cierta lógica de coherencia para asegurarse de que se configuran los elementos de forma razonable. Esta lógica se puede implementar de dos maneras, como se indica a continuación:

-   **Dependencias.** Es posible que no pueda realizar algunos cambios porque otra propiedad depende de un valor determinado para una propiedad que se intenta establecer. Por ejemplo, si un componente se establece con las transacciones de atributo necesarias y, a continuación, intenta cambiar la configuración de sincronización a ninguno, se genera un error al intentar llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) porque las transacciones dependen de la sincronización.
-   **Efectos secundarios.** Es posible que algunas propiedades se cambien automáticamente sin que las establezca explícitamente. Por ejemplo, si establece un componente con las transacciones de atributo necesarias, la sincronización se establecerá también en requerido. En realidad, es el lado de volteo de las dependencias: una propiedad tiene prioridad sobre otra, y su dependencia se expresa mediante el establecimiento de la propiedad secundaria y el bloqueo de los cambios en ella.

En la lista de propiedades expuestas por los elementos de una colección, todas enumeradas en [colecciones de administración de com+](com--administration-collections.md), se indican las dependencias y los efectos secundarios para cada propiedad. Al configurar aplicaciones y componentes COM+, debe tener en cuenta las restricciones que se imponen en las configuraciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Consultar las propiedades disponibles](querying-for-available-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



