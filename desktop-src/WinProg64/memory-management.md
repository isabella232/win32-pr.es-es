---
title: Administración de memoria en WOW64
description: La administración de memoria bajo WOW64 depende de la arquitectura del procesador.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 bits programación de Windows, administración de memoria
- Administración de memoria 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421273"
---
# <a name="memory-management-under-wow64"></a>Administración de memoria en WOW64

La administración de memoria bajo WOW64 depende de la arquitectura del procesador.

## <a name="itanium-support"></a>Compatibilidad con Itanium

WOW64 simula páginas de 4 KB sobre las páginas nativas de 8 KB que usa el procesador Itanium. El procesador ayuda a proporcionar una simulación excelente con poca sobrecarga. El código de simulación no puede controlar los siguientes casos:

-   Seguimiento de escritura. Las funciones [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) y [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) se implementan en el kernel con la granularidad de tamaño de página nativa, lo que significa que la simulación de páginas de WOW64 de 4 KB no puede determinar qué páginas de 4 KB simuladas se escriben en la página de 8 KB subyacente.
-   [Extensiones de ventana de dirección (AWE)](/windows/desktop/Memory/address-windowing-extensions). Las funciones AWE operan en números de página y no hay forma de asignar números de página de 64 bits a números de página de 32 bits.
-   Alineación de la sección. En el caso de las imágenes ejecutables con una alineación de sección inferior a 8 KB (el valor predeterminado es 4 KB para imágenes x86), WOW64 debe haber modificado todas las páginas de imagen. Esto copia eficazmente cada página en el archivo de paginación y evita que las páginas de imagen de solo lectura se compartan entre los procesos.
-   No se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) y [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .

## <a name="x64-and-arm64-support"></a>Compatibilidad con x64 y ARM64

El tamaño de página nativo es 4 KB. Por lo tanto, se admite lo siguiente:

-   Se admiten las funciones [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) y [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .
-   Se admiten las funciones [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) y [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .
-   El uso de direcciones grandes tiene ventajas porque x64 WOW64 admite un espacio de direcciones virtuales de 4 GB.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de memoria para las versiones de Windows](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Optimización de la RAM de 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 