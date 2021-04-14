---
description: Obtener y establecer propiedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtener y establecer propiedades (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496337"
---
# <a name="getting-and-setting-properties-component-services"></a>Obtener y establecer propiedades (servicios de componentes)

Para poder leer o escribir propiedades concretas expuestas por un elemento de una colección, debe realizar los siguientes pasos:

1.  Recupere la colección.
2.  Rellene la colección para leer los datos del catálogo de COM+.
3.  Recupere el elemento específico de la colección, que lo representa con un objeto de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Para obtener un ejemplo en el que se ilustran estos pasos, consulte [navegar por la jerarquía de la colección de com+](navigating-the-com--collection-hierarchy.md).

Dado que las propiedades concretas expuestas pueden variar en función de lo que representa el elemento; es decir, un elemento que representa un componente tiene propiedades diferentes de las que representan una aplicación COM+. Establezca cualquiera de estas propiedades mediante una única propiedad genérica, la propiedad Value, en [**COMAdminCatalogObject**](comadmincatalogobject.md).

La propiedad Value permite obtener o establecer cualquier propiedad con nombre específica expuesta por un elemento, devolver un valor para una propiedad con nombre al obtener y tomar un nombre y un valor al establecer.

En realidad, no se registra ningún cambio en el catálogo de COM+ hasta que no se guardan explícitamente los cambios mediante el método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Los cambios pendientes de todas las propiedades de todos los elementos de una colección determinada se guardan de una vez. Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).

No se aceptarán todos los cambios que realice. El catálogo de COM+ exige cierta lógica de coherencia para asegurarse de que se configuran de forma razonable. Además, al cambiar algunas propiedades, otras podrían cambiar automáticamente por la misma lógica de coherencia. Estos efectos aparecen al intentar guardar los cambios.

> [!Note]  
> Es posible que tenga contención con otro escritor en el catálogo de COM+. Entre las llamadas a [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección determinada, no hay ningún bloqueo en ninguno de los datos del catálogo. Es posible que varias partes estén configurando los elementos de forma simultánea en una colección determinada y que puedan estar subiendo al guardar los cambios. Esto significa que otra persona podría cambiar la configuración de un objeto antes o después de hacerlo, ya sea mediante la ejecución de algún tipo de programa con los objetos COMAdmin o mediante la herramienta administrativa Servicios de componentes, ya sea de forma local o remota. La regla general con la escritura de objetos en el catálogo es que todas las propiedades de un objeto se escriben a la vez. Es decir, el último escritor gana: el objeto se guarda en el catálogo exactamente como el último escritor lo configuró.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Consultar las propiedades disponibles](querying-for-available-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



