---
title: Rendimiento y consumo de memoria en WOW64
description: El rendimiento y el consumo de memoria en WOW64 se determinan según los siguientes factores.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- rendimiento en la programación de Windows en WOW64 64 bits
- consumo de memoria bajo WOW64 64 de programación de Windows
- WOW64 de 64 bits programación de Windows, rendimiento
- WOW64 64 bits programación de Windows, consumo de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421272"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Rendimiento y consumo de memoria en WOW64

El rendimiento y el consumo de memoria en WOW64 vienen determinados por los siguientes factores:

-   Hardware del procesador. La emulación de instrucciones se realiza en el chip. En el procesador x64, el procesador ejecuta de forma nativa las instrucciones x86. Por lo tanto, la velocidad de ejecución en WOW64 en x64 es similar a la velocidad en Windows de 32 bits. En el procesador Intel Itanium y en todos los procesadores ARM64, hay más software implicado en la emulación y el rendimiento se ve afectado.
-   Sobrecarga de thunk de API. Esta sobrecarga es pequeña en comparación con las llamadas del sistema al kernel de NT. Las funciones de kernel de NT están diseñadas para que se llamen con poca frecuencia.
-   Tamaño de la memoria virtual. En el procesador Intel Itanium, WOW64 agrega una sobrecarga significativa si dos o más instancias de la misma aplicación de 32 bits se ejecutan simultáneamente. Esto se debe a las páginas nativas de 8 KB en Intel Itanium, que complica la emulación de las páginas nativas de 4 KB en la arquitectura x86 (más páginas se marcan como modificables; todas las páginas que se pueden escribir son privadas en el proceso). Esto puede afectar negativamente a la escalabilidad de Terminal Services en determinados procesadores. Este no es el caso del procesador x64.
-   Espacio de trabajo. WOW64 aumenta el tamaño del espacio de trabajo de la aplicación.

WOW64 permite que las aplicaciones de 32 bits aprovechen el kernel de 64 bits. Por lo tanto, las aplicaciones de 32 bits pueden usar un mayor número de identificadores de kernel y de ventana. Sin embargo, es posible que las aplicaciones de 32 bits no puedan crear tantos subprocesos en WOW64 como se ejecuten de forma nativa en sistemas basados en x86, porque WOW64 asigna una pila de 64 bits adicional (normalmente 512 KB) para cada subproceso. Además, se reserva una cantidad de espacio de direcciones para el propio WOW64 y las estructuras de datos que usa. La cantidad reservada depende del procesador; hay más reservada en Intel Itanium que en los procesadores x64 o ARM64.

Si la aplicación tiene el [**indicador \_ \_ reconocimiento de \_ direcciones \_ grandes del archivo de imagen**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) establecido en el encabezado de la imagen, cada aplicación de 32 bits recibirá 4 GB de espacio de direcciones virtuales en el entorno WOW64. Si no se establece la marca **\_ \_ \_ \_ reconocimiento de direcciones grandes del archivo de imagen** , cada aplicación de 32 bits recibe 2 GB de espacio de direcciones virtuales en el entorno WOW64.

 

 