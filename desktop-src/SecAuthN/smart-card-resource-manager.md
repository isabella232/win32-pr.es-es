---
description: Administrador de recursos de tarjeta inteligente
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Administrador de recursos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668257"
---
# <a name="smart-card-resource-manager"></a>Administrador de recursos de tarjeta inteligente

El [*Administrador de recursos*](../secgloss/r-gly.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) administra el acceso a los [*lectores*](../secgloss/r-gly.md) y a las *tarjetas inteligentes*. Para administrar estos recursos, realiza las siguientes funciones.

-   Identifica y realiza un seguimiento de los recursos.
-   Asigna lectores y recursos entre varias aplicaciones.
-   Admite primitivas de [*transacción*](../secgloss/t-gly.md) para tener acceso a los servicios disponibles en una tarjeta determinada.
    > [!Note]  
    > Este es un punto importante porque las tarjetas actuales son dispositivos de un solo subproceso, que a menudo requieren la ejecución de varios comandos para completar una sola función. [*Las transacciones*](../secgloss/t-gly.md) permiten que se ejecuten varios comandos sin interrupción, lo que garantiza que la información de [*Estado*](../secgloss/s-gly.md) intermedio no esté dañada.

     

Se puede acceder directamente al administrador de recursos mediante la API de Resource Manager o indirectamente a través de cualquier [*proveedor de servicios*](../secgloss/s-gly.md)de tarjetas inteligentes.

La API de Resource Manager es un conjunto de funciones de Windows que proporcionan acceso directo a los servicios del administrador de recursos. Para obtener información general sobre las funciones de Windows proporcionadas por la API, consulte [API de administrador de recursos de tarjetas inteligentes](smart-card-resource-manager-api.md). En comparación, los proveedores de servicios de tarjetas inteligentes usan interfaces COM.

Muchas de las funciones de Windows de la API de Resource Manager tienen equivalentes en las propiedades y los métodos de las interfaces COM de los proveedores de servicios de tarjetas inteligentes. Además, aunque la mayoría de los desarrolladores de aplicaciones encontrarán que COM es más fácil de trabajar con, algunas aplicaciones seguirán necesitando usar las funciones de Windows para realizar determinadas tareas. Por ejemplo, las aplicaciones que necesitan manipular la lista de lectores o grupos de lectores en la [*base de datos de tarjetas inteligentes*](../secgloss/s-gly.md), y las que necesitan el control directo de un lector, deben usar la API de Resource Manager. Los servicios que proporcionan estas funciones solo están disponibles en las funciones de Windows, no en el COM proporcionado por los proveedores de servicios.

Para obtener información sobre cómo se implementa el [*Administrador de recursos*](../secgloss/r-gly.md) en Windows, consulte [Administrador de recursos implementación](resource-manager-implementation.md).

 

 
