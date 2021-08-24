---
title: Rendimiento y consumo de memoria en WOW64
description: El rendimiento y el consumo de memoria en WOW64 están determinados por los siguientes factores.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- rendimiento en WOW64 de 64 bits Windows programación
- consumo de memoria en WOW64 de 64 bits Windows programación
- WOW64 de 64 bits Windows programación , rendimiento
- WOW64 64 bits de programación Windows, consumo de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d5dd20cb42245318bf2666da788b9eea9e371c3945155c1b03b876fa513f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613835"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Rendimiento y consumo de memoria en WOW64

El rendimiento y el consumo de memoria en WOW64 están determinados por los siguientes factores:

-   Hardware del procesador. La emulación de instrucciones se realiza en el chip. En el procesador x64, el procesador ejecuta de forma nativa las instrucciones x86. Por lo tanto, la velocidad de ejecución en WOW64 en x64 es similar a su velocidad por debajo de 32 bits Windows. En el procesador Intel Itanium y cualquier procesador ARM64, hay más software implicado en la emulación y el rendimiento se sufre como resultado.
-   Sobrecarga de thunk de API. Esta sobrecarga es pequeña en comparación con las llamadas del sistema al kernel nt. Las funciones de kernel nt están diseñadas para llamarse con poca frecuencia.
-   Tamaño de memoria virtual. En el procesador Intel Itanium, WOW64 agrega una sobrecarga significativa si dos o más instancias de la misma aplicación de 32 bits se ejecutan simultáneamente. Esto se debe a las páginas nativas de 8 KB en Intel Itanium, lo que complica la emulación de las páginas nativas de 4 KB en la arquitectura x86 (hay más páginas marcadas como grabables; todas las páginas que se pueden escribir son privadas para el proceso). Esto puede afectar negativamente a la escalabilidad de Terminal Services en determinados procesadores. Este no es el caso del procesador x64.
-   Conjunto de trabajo. WOW64 aumenta el tamaño del conjunto de trabajo de la aplicación.

WOW64 permite que las aplicaciones de 32 bits aprovechen el kernel de 64 bits. Por lo tanto, las aplicaciones de 32 bits pueden usar un mayor número de identificadores de kernel y identificadores de ventana. Sin embargo, es posible que las aplicaciones de 32 bits no puedan crear tantos subprocesos en WOW64 como puedan al ejecutarse de forma nativa en sistemas basados en x86 porque WOW64 asigna una pila de 64 bits adicional (normalmente 512 KB) para cada subproceso. Además, se reserva cierta cantidad de espacio de direcciones para WOW64 y las estructuras de datos que usa. La cantidad reservada depende del procesador; se reserva más en Intel Itanium que en los procesadores x64 o ARM64.

Si la aplicación tiene la marca [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) establecida en el encabezado de imagen, cada aplicación de 32 bits recibe 4 GB de espacio de direcciones virtuales en el entorno WOW64. Si la **marca IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** no está establecida, cada aplicación de 32 bits recibe 2 GB de espacio de direcciones virtuales en el entorno WOW64.

 

 