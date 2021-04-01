---
description: La agrupación de aplicaciones COM+ permite escalar los procesos de un solo subproceso, de manera similar a la forma en que la agrupación de subprocesos permite escalar objetos de un solo subproceso.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceptos de agrupación de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907103"
---
# <a name="com-application-pooling-concepts"></a>Conceptos de agrupación de aplicaciones COM+

La agrupación de aplicaciones COM+ permite escalar los procesos de un solo subproceso, de manera similar a la forma en que la agrupación de subprocesos permite escalar objetos de un solo subproceso. La agrupación de aplicaciones también puede ayudar a recuperarse de los errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.

> [!Note]  
> Las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

Todos los métodos de la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) admiten la agrupación de aplicaciones.

La agrupación de aplicaciones COM+ se puede configurar por aplicación mediante la propiedad ConcurrentApps del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) en la colección de [**aplicaciones**](applications.md) . ConcurrentApps es un valor entero que especifica el número máximo de procesos Dllhost simultáneos que deben iniciarse para realizar activaciones de servicio para una aplicación. Esta propiedad se puede establecer mediante la herramienta de administración de servicios de componentes o mediante programación.

Si la propiedad ConcurrentApps se establece en 1, que es el valor predeterminado, se deshabilita el servicio de agrupación de aplicaciones COM+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de agrupación de aplicaciones COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Conceptos de reciclaje de aplicaciones COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



