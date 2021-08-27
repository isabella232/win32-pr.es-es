---
description: La agrupación de aplicaciones COM+ permite escalar procesos de un solo subproceso, de forma similar a la manera en que la agrupación de subprocesos permite escalar objetos de un solo subproceso.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceptos de agrupación de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aab46350e3c6084c0d5e8ca61d2f3c90d27e06795f7d08568ee4a7c1e0fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096915"
---
# <a name="com-application-pooling-concepts"></a>Conceptos de agrupación de aplicaciones COM+

La agrupación de aplicaciones COM+ permite escalar procesos de un solo subproceso, de forma similar a la manera en que la agrupación de subprocesos permite escalar objetos de un solo subproceso. La agrupación de aplicaciones también puede ayudar a recuperarse de errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.

> [!Note]  
> Las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

Todos los métodos de la [**interfaz ICOMAdminCatalog2 admiten**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) la agrupación de aplicaciones.

La agrupación de aplicaciones COM+ se puede configurar por aplicación mediante la propiedad ConcurrentApps del [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) de la [**colección Applications.**](applications.md) ConcurrentApps es un valor entero que especifica el número máximo de procesos dllhost simultáneos que se deben iniciar para dar servicio a las activaciones de una aplicación. Esta propiedad se puede establecer mediante la herramienta de administración servicios de componentes o mediante programación.

Si la propiedad ConcurrentApps está establecida en 1, que es el valor predeterminado, el servicio de agrupación de aplicaciones COM+ está deshabilitado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de agrupación de aplicaciones COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Conceptos de reciclaje de aplicaciones COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



