---
description: La agrupación de aplicaciones COM+ permite escalar procesos de un solo subproceso, de forma similar a la forma en que la agrupación de subprocesos permite escalar objetos de subproceso único.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceptos de agrupación de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973557"
---
# <a name="com-application-pooling-concepts"></a>Conceptos de agrupación de aplicaciones COM+

La agrupación de aplicaciones COM+ permite escalar procesos de un solo subproceso, de forma similar a la forma en que la agrupación de subprocesos permite escalar objetos de subproceso único. La agrupación de aplicaciones también puede ayudar a recuperarse de errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.

> [!Note]  
> Las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

Todos los métodos de la [**interfaz ICOMAdminCatalog2 admiten**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) la agrupación de aplicaciones.

La agrupación de aplicaciones COM+ se puede configurar por aplicación mediante la propiedad ConcurrentApps del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la [**colección Applications.**](applications.md) ConcurrentApps es un valor entero que especifica el número máximo de procesos dllhost simultáneos que se deben iniciar para dar servicio a las activaciones de una aplicación. Esta propiedad se puede establecer mediante la herramienta de administración servicios de componentes o mediante programación.

Si la propiedad ConcurrentApps se establece en 1, que es el valor predeterminado, el servicio de agrupación de aplicaciones COM+ está deshabilitado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de agrupación de aplicaciones COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Conceptos de reciclaje de aplicaciones COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



