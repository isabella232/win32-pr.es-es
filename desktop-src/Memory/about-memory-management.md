---
description: Cada proceso de 32 bits de Microsoft Windows tiene su propio espacio de direcciones virtuales que permite el direccionamiento de hasta 4 gigabytes de memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Acerca de la administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159902"
---
# <a name="about-memory-management"></a>Acerca de la administración de memoria

Cada proceso de 32 bits de Microsoft Windows tiene su propio espacio de direcciones virtuales que permite el direccionamiento de hasta 4 gigabytes de memoria. Cada proceso de 64 bits Windows un espacio de direcciones virtual de 8 terabytes. Todos los subprocesos de un proceso pueden acceder a su espacio de direcciones virtuales. Sin embargo, los subprocesos no pueden acceder a la memoria que pertenece a otro proceso, lo que protege a un proceso de que otro proceso los da por dañado.

Para obtener información sobre el espacio de direcciones virtuales y las funciones de administración de memoria, consulte los temas siguientes.

-   [Espacio de direcciones virtuales](virtual-address-space.md)
-   [Grupos de memoria](memory-pools.md)
-   [Información de rendimiento de memoria](memory-performance-information.md)
-   [Funciones de memoria virtual](virtual-memory-functions.md)
-   [Funciones del montón](heap-functions.md)
-   [Asignación de archivos](file-mapping.md)
-   [Compatibilidad con memoria grande](large-memory-support.md)
-   [Funciones globales y locales](global-and-local-functions.md)
-   [Funciones de la biblioteca estándar de C](standard-c-library-functions.md)
-   [Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)

 

 



