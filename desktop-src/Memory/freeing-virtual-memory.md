---
description: La función VirtualFree desasocupa y libera páginas según las reglas siguientes.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Liberar memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159863"
---
# <a name="freeing-virtual-memory"></a>Liberar memoria virtual

La [**función VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) desasocupa y libera páginas según las reglas siguientes:

-   Desacomprime una o varias páginas confirmadas, cambiando el estado de las páginas a reservadas. La desasignación de páginas libera el almacenamiento físico asociado a las páginas, lo que hace que esté disponible para que lo asigne cualquier proceso. Cualquier bloque de páginas confirmadas se puede desa confirmar.
-   Libera un bloque de una o varias páginas reservadas, cambiando el estado de las páginas a libre. Al liberar un bloque de páginas, el intervalo de direcciones reservadas está disponible para que el proceso lo asigne. Las páginas reservadas solo se pueden liberar liberando todo el bloque que [**virtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)ha reservado inicialmente.
-   Desafila y libera un bloque de una o varias páginas confirmadas simultáneamente, cambiando el estado de las páginas a libre. El bloque especificado debe incluir todo el bloque reservado inicialmente por [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)y todas las páginas deben estar actualmente confirmadas.

Una vez que se libera o se desencomprime un bloque de memoria, nunca se puede volver a hacer referencia a él. Cualquier información que pueda haber estado en esa memoria ha desaparecido para siempre. Al intentar leer o escribir en una página gratuita, se produce una excepción de infracción de acceso. Si necesita información, no desacomprima ni libre memoria que contenga esa información.

Para especificar que los datos de un intervalo de memoria ya no son de interés, llame a [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) con **MEM \_ RESET**. Las páginas no se leerán ni escribirán en el archivo de paginación. Sin embargo, el bloque de memoria se puede usar de nuevo más adelante.

 

 
