---
description: La función VirtualFree desconfirma y libera las páginas de acuerdo con las reglas siguientes.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Liberar memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677358"
---
# <a name="freeing-virtual-memory"></a>Liberar memoria virtual

La función [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) desconfirma y libera las páginas según las siguientes reglas:

-   Anula la confirmación de una o varias páginas confirmadas, lo que cambia el estado de las páginas a reservado. La desactivación de páginas libera el almacenamiento físico asociado con las páginas, lo que hace que esté disponible para que lo asigne cualquier proceso. Cualquier bloque de páginas confirmadas se puede desasignar.
-   Libera un bloque de una o varias páginas reservadas, lo que cambia el estado de las páginas a gratis. Al liberar un bloque de páginas, el proceso puede asignar el intervalo de direcciones reservadas. Las páginas reservadas solo se pueden liberar liberando todo el bloque que ha reservado inicialmente [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   Desconfirma y libera un bloque de una o varias páginas confirmadas simultáneamente, lo que cambia el estado de las páginas a gratis. El bloque especificado debe incluir el bloque completo inicialmente reservado por [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)y todas las páginas deben estar confirmadas actualmente.

Después de liberar o desasignar un bloque de memoria, nunca puede hacer referencia a él de nuevo. Toda la información que pueda haber estado en esa memoria quedará indefinidamente. Al intentar leer o escribir en una página libre, se produce una excepción de infracción de acceso. Si necesita información, no desconfirme ni libere memoria que contenga esa información.

Para especificar que los datos de un intervalo de memoria ya no son de interés, llame a [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) con el **\_ restablecimiento** de memoria. Las páginas no se leerán ni se escribirán en el archivo de paginación. Sin embargo, el bloque de memoria se puede volver a usar más adelante.

 

 
