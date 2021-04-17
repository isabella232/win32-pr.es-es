---
description: La compatibilidad con páginas de gran tamaño permite a las aplicaciones de servidor establecer regiones de memoria de gran tamaño, lo que es especialmente útil en Windows de 64 bits.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Compatibilidad con Large-Page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677401"
---
# <a name="large-page-support"></a>Compatibilidad con Large-Page

La compatibilidad con páginas de gran tamaño permite a las aplicaciones de servidor establecer regiones de memoria de gran tamaño, lo que es especialmente útil en Windows de 64 bits. Cada traducción de página grande utiliza un único búfer de traducción dentro de la CPU. El tamaño de este búfer suele ser tres pedidos de magnitud mayor que el tamaño de página nativo; Esto aumenta la eficacia del búfer de traducción, lo que puede aumentar el rendimiento de la memoria a la que se accede con frecuencia.

En el procedimiento siguiente se describe cómo usar la compatibilidad con páginas de gran tamaño.

**Para usar la compatibilidad con páginas grandes**

1.  Obtenga el privilegio **SeLockMemoryPrivilege** mediante una llamada a la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) . Para obtener más información, consulte [asignación de privilegios a una cuenta](../secbp/assigning-privileges-to-an-account.md) y [cambio de privilegios en un token](../secbp/changing-privileges-in-a-token.md).
2.  Recupere el tamaño mínimo de página grande mediante una llamada a la función [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .
3.  Incluya el valor de **MEM \_ Large \_ pages** al llamar a la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) . El tamaño y la alineación deben ser un múltiplo del mínimo de la página grande.

Al escribir aplicaciones que utilizan memoria de página grande, tenga en cuenta las consideraciones siguientes:

-   Las regiones de memoria de gran tamaño pueden resultar difíciles de obtener después de que el sistema se ejecute durante mucho tiempo, ya que el espacio físico para cada página grande debe ser contiguo, pero es posible que se haya fragmentado la memoria. Asignar páginas grandes en estas condiciones puede afectar significativamente al rendimiento del sistema. Por lo tanto, las aplicaciones deben evitar que se repitan las asignaciones de páginas grandes y, en su lugar, asignar todas las páginas grandes una vez, en el inicio.
-   La memoria es siempre de lectura/escritura y no paginable (siempre residente en la memoria física).
-   La memoria forma parte de los bytes privados del proceso pero no de parte del espacio de trabajo, porque el espacio de trabajo establecido por definición contiene solo memoria paginable.
-   Las asignaciones de páginas grandes no están sujetas a límites de trabajos.
-   La memoria de páginas grandes debe estar reservada y confirmada como una sola operación. En otras palabras, las páginas grandes no se pueden usar para confirmar un intervalo de memoria reservado previamente.
-   WOW64 en sistemas basados en Intel Itanium no admite aplicaciones de 32 bits que usan esta característica. Las aplicaciones deben volver a compilarse como aplicaciones nativas de 64 bits.

 

 
