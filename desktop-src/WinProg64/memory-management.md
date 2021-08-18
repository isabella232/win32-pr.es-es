---
title: Administración de memoria en WOW64
description: La administración de memoria en WOW64 depende de la arquitectura del procesador.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 bits de programación Windows , administración de memoria
- administración de memoria de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132838"
---
# <a name="memory-management-under-wow64"></a>Administración de memoria en WOW64

La administración de memoria en WOW64 depende de la arquitectura del procesador.

## <a name="itanium-support"></a>Compatibilidad con Itanium

WOW64 simula páginas de 4 KB sobre las páginas nativas de 8 KB que usa el procesador Itanium. El procesador ayuda al proporcionar una simulación excelente con poca sobrecarga. El código de simulación no puede controlar los casos siguientes:

-   Seguimiento de escritura. Las funciones [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) y [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) se implementan en el kernel mediante granularidad de tamaño de página nativa, lo que significa que la simulación de página wow64 de 4 KB no puede determinar qué páginas simuladas de 4 KB se escriben en la página subyacente de 8 KB.
-   [Extensiones de ventana de direcciones (AWE).](/windows/desktop/Memory/address-windowing-extensions) Las funciones de AWE funcionan en números de página y no hay ninguna manera de asignar números de página de 64 bits a números de página de 32 bits.
-   Alineación de sección. En el caso de las imágenes ejecutables con alineación de sección inferior a 8 KB (el valor predeterminado es 4 KB para imágenes x86), WOW64 debe ensuciar todas las páginas de imágenes. Esto copia de forma eficaz cada página en el archivo de página e impide que las páginas de imagen de solo lectura se compartan entre procesos.
-   No se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) y [**WriteFileGather.**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather)

## <a name="x64-and-arm64-support"></a>Compatibilidad con x64 y ARM64

El tamaño de página nativo es de 4 KB. Por lo tanto, se admite lo siguiente:

-   Se [**admiten las funciones GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) [**y ResetWriteWatch.**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch)
-   Se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) [**y WriteFileGather.**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather)
-   El uso de direcciones grandes tiene ventajas porque x64 WOW64 admite un espacio de direcciones virtuales de 4 GB.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de memoria para Windows versiones anteriores](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Ajuste de RAM de 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 