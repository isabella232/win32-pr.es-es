---
description: Interdependencias entre propiedades
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdependencias entre propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb039db26ee06868da0b1832e1a3af2692ac47cde73bf7fe5c2e934916c4f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547690"
---
# <a name="interdependencies-between-properties"></a>Interdependencias entre propiedades

Al establecer propiedades, el catálogo de COM+ aplica cierta lógica de coherencia para asegurarse de que se configuran los elementos de una manera razonable. Esta lógica se puede implementar de dos maneras, como se muestra a continuación:

-   **Dependencias.** Es posible que se le bloquee la realización de algunos cambios porque otra propiedad depende de una configuración determinada para una propiedad que intenta establecer. Por ejemplo, si se establece un componente con el atributo Transacciones necesarias y, a continuación, intenta cambiar la configuración de sincronización a Ninguno, se genera un error al intentar llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) porque las transacciones dependen de la sincronización.
-   **Efectos secundarios.** Es posible que algunas propiedades se cambien automáticamente sin establecerlas explícitamente. Por ejemplo, si establece un componente con el atributo Transacciones necesarias, la sincronización también se establecerá en Requerido. Este es realmente el lado opuesto de las dependencias: una propiedad tiene prioridad sobre otra y su dependencia se expresa primero estableciendo la propiedad secundaria y bloqueando los cambios en ella.

En la lista de propiedades expuestas por elementos de una colección, todas enumeradas en Colecciones de administración de [COM+,](com--administration-collections.md)se indican las dependencias y los efectos secundarios para cada propiedad. Al configurar componentes y aplicaciones COM+, debe tener en cuenta qué restricciones se imponen en las configuraciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Consulta de propiedades disponibles](querying-for-available-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



