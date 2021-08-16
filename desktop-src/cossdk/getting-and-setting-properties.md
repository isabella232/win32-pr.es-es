---
description: Obtener y establecer propiedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtener y establecer propiedades (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805d98463e1f9b8f08c1018b49554c95e2735bfa7ea6dca21d90243eb324df49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306760"
---
# <a name="getting-and-setting-properties-component-services"></a>Obtener y establecer propiedades (servicios de componentes)

Para poder leer o escribir propiedades concretas expuestas por un elemento de una colección, debe realizar los pasos siguientes:

1.  Recupere la colección.
2.  Rellene la colección para leer los datos del catálogo de COM+.
3.  Recupere el elemento específico de la colección, que lo representa con un objeto de la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md)

Para obtener un ejemplo que ilustra estos pasos, vea [Navegar por la jerarquía de colecciones de COM+.](navigating-the-com--collection-hierarchy.md)

Dado que las propiedades concretas expuestas pueden variar en función de lo que represente el elemento; Es decir, un elemento que representa un componente tiene propiedades diferentes de una que representa una aplicación COM+. Establezca cualquiera de estas propiedades mediante una sola propiedad genérica, la propiedad Value, en [**COMAdminCatalogObject**](comadmincatalogobject.md).

La propiedad Value permite obtener o establecer cualquier propiedad con nombre específica expuesta por un elemento, devolviendo un valor para una propiedad con nombre al obtener y tomando un nombre y un valor al establecer.

No se registra ningún cambio en el catálogo de COM+ hasta que guarde explícitamente los cambios mediante el [**método SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md) Los cambios pendientes para todas las propiedades de todos los elementos de una colección determinada se guardan a la vez. Para obtener más información, [vea Guardar o descartar cambios.](saving-or-discarding-changes.md)

No se aceptarán todos los cambios que realice. El catálogo de COM+ aplica cierta lógica de coherencia para asegurarse de que se configuran las cosas de una manera razonable. Además, al cambiar algunas propiedades, otras pueden cambiar automáticamente por la misma lógica de coherencia. Estos efectos se muestran al intentar guardar los cambios.

> [!Note]  
> Es posible que esté en contención con otro escritor en el catálogo de COM+. Entre las llamadas [**a Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección determinada, no tiene ningún bloqueo en ninguno de los datos del catálogo. Es posible que varias partes configuren simultáneamente elementos en una colección determinada y puedan estar en contra cuando guarden los cambios. Esto significa que otra persona podría cambiar la configuración de un objeto antes o después de hacerlo, ya sea ejecutando algún tipo de programa mediante los objetos COMAdmin o mediante la herramienta administrativa Servicios de componentes, ya sea de forma local o remota. La regla general con la escritura de objetos en el catálogo es que todas las propiedades de un objeto se escriben a la vez. Es decir, el último escritor gana: el objeto se guarda en el catálogo exactamente como lo configuró el último escritor.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Consulta de propiedades disponibles](querying-for-available-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



