---
description: Tarjeta inteligente Resource Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Tarjeta inteligente Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9d78b1d54a4db3fa8146b2689173c264e8320da024d0dc3e165dd648b8a33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917514"
---
# <a name="smart-card-resource-manager"></a>Tarjeta inteligente Resource Manager

El [*administrador de recursos*](../secgloss/s-gly.md) de [*tarjeta*](../secgloss/r-gly.md) inteligente administra el acceso a los [*lectores*](../secgloss/r-gly.md) y a *las tarjetas inteligentes.* Para administrar estos recursos, realiza las siguientes funciones.

-   Identifica y realiza un seguimiento de los recursos.
-   Asigna lectores y recursos en varias aplicaciones.
-   Admite [*primitivas*](../secgloss/t-gly.md) de transacción para acceder a los servicios disponibles en una tarjeta determinada.
    > [!Note]  
    > Este es un punto importante porque las tarjetas actuales son dispositivos de un solo subproceso que a menudo requieren la ejecución de varios comandos para completar una sola función. [*Las transacciones*](../secgloss/t-gly.md) permiten ejecutar varios comandos sin interrupción, lo que garantiza que la [*información*](../secgloss/s-gly.md) de estado intermedio no esté dañada.

     

Se puede acceder al administrador de recursos directamente mediante la API de Resource Manager o indirectamente a través de cualquier proveedor de servicios de [*tarjeta inteligente.*](../secgloss/s-gly.md)

La API de Resource Manager es un conjunto de Windows que proporcionan acceso directo a los servicios del administrador de recursos. Para obtener información general sobre las funciones Windows proporcionadas por la API, consulte [Smart Card Resource Manager API](smart-card-resource-manager-api.md). En comparación, los proveedores de servicios de tarjeta inteligente usan interfaces COM.

Muchas de las Windows en la API de Resource Manager tienen equivalentes en las propiedades y métodos de las interfaces COM de los proveedores de servicios de tarjeta inteligente. Y aunque a la mayoría de los desarrolladores de aplicaciones les será más fácil trabajar con COM, algunas aplicaciones seguirán necesitando usar las funciones de Windows para realizar ciertas tareas. Por ejemplo, las aplicaciones que necesitan manipular la [](../secgloss/s-gly.md)lista de lectores o grupos de lectores de la base de datos de tarjetas inteligentes y las que necesitan el control directo de un lector, deben usar la API de Resource Manager. Los servicios que proporcionan estas funcionalidades solo están disponibles en las Windows, no en el COM proporcionado por los proveedores de servicios.

Para obtener información sobre cómo se implementa [*resource manager*](../secgloss/r-gly.md) en Windows, consulte Resource Manager [implementación de](resource-manager-implementation.md).

 

 
