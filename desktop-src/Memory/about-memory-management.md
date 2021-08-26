---
description: Cada proceso en Microsoft Windows de 32 bits tiene su propio espacio de direcciones virtuales que permite el direccionamiento de hasta 4 gigabytes de memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Acerca de la administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869975"
---
# <a name="about-memory-management"></a>Acerca de la administración de memoria

Cada proceso en Microsoft Windows de 32 bits tiene su propio espacio de direcciones virtuales que permite el direccionamiento de hasta 4 gigabytes de memoria. Cada proceso de 64 bits Windows un espacio de direcciones virtuales de 8 terabytes. Todos los subprocesos de un proceso pueden acceder a su espacio de direcciones virtuales. Sin embargo, los subprocesos no pueden acceder a la memoria que pertenece a otro proceso, lo que protege a un proceso de que otro proceso los da dañado.

Para obtener información sobre el espacio de direcciones virtuales y las funciones de administración de memoria, consulte los temas siguientes.

-   [Espacio de direcciones virtuales](virtual-address-space.md)
-   [Grupos de memoria](memory-pools.md)
-   [Información de rendimiento de memoria](memory-performance-information.md)
-   [Funciones de memoria virtual](virtual-memory-functions.md)
-   [Funciones de montón](heap-functions.md)
-   [Asignación de archivos](file-mapping.md)
-   [Compatibilidad con memoria grande](large-memory-support.md)
-   [Funciones globales y locales](global-and-local-functions.md)
-   [Funciones de la biblioteca estándar de C](standard-c-library-functions.md)
-   [Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)

 

 



