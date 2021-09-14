---
description: La compatibilidad con páginas grandes permite que las aplicaciones de servidor establezcan regiones de memoria de página grande, lo que resulta especialmente útil en las aplicaciones de 64 Windows.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page soporte técnico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159852"
---
# <a name="large-page-support"></a>Large-Page soporte técnico

La compatibilidad con páginas grandes permite que las aplicaciones de servidor establezcan regiones de memoria de página grande, lo que resulta especialmente útil en las aplicaciones de 64 Windows. Cada traducción de página grande usa un único búfer de traducción dentro de la CPU. El tamaño de este búfer suele ser de tres órdenes de magnitud mayor que el tamaño de página nativo; Esto aumenta la eficacia del búfer de traducción, que puede aumentar el rendimiento de la memoria a la que se accede con frecuencia.

En el procedimiento siguiente se describe cómo usar la compatibilidad con páginas grandes.

**Para usar la compatibilidad con páginas grandes**

1.  Obtenga el **privilegio SeLockMemoryPrivilege** llamando a la [**función AdjustTokenPrivileges.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) Para obtener más información, vea [Asignación de privilegios](../secbp/assigning-privileges-to-an-account.md) a una cuenta y [Cambio de privilegios en un token.](../secbp/changing-privileges-in-a-token.md)
2.  Recupere el tamaño mínimo de página grande llamando a [**la función GetLargePageMinimum.**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum)
3.  Incluya el **valor \_ DE MEM LARGE \_ PAGES** al llamar a la [**función VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) El tamaño y la alineación deben ser un múltiplo del mínimo de página grande.

Al escribir aplicaciones que usan memoria de página grande, tenga en cuenta las siguientes consideraciones:

-   Las regiones de memoria de página grande pueden ser difíciles de obtener después de que el sistema se haya estado ejecutando durante mucho tiempo porque el espacio físico de cada página grande debe ser contiguo, pero es posible que la memoria se haya fragmentado. La asignación de páginas grandes en estas condiciones puede afectar significativamente al rendimiento del sistema. Por lo tanto, las aplicaciones deben evitar realizar asignaciones repetidas de páginas grandes y, en su lugar, asignar todas las páginas grandes una vez, en el inicio.
-   La memoria siempre es de lectura/escritura y no se puede páginas (siempre residen en la memoria física).
-   La memoria forma parte del proceso de bytes privados, pero no forma parte del espacio de trabajo, porque el espacio de trabajo por definición contiene solo memoria paginable.
-   Las asignaciones de páginas grandes no están sujetas a límites de trabajo.
-   La memoria de página grande se debe reservar y confirmado como una sola operación. En otras palabras, no se pueden usar páginas grandes para confirmar un intervalo de memoria previamente reservado.
-   WOW64 en sistemas basados en Intel Itanium no admite aplicaciones de 32 bits que usen esta característica. Las aplicaciones se deben volver a compilar como aplicaciones nativas de 64 bits.

 

 
