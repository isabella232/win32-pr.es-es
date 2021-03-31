---
title: Guía de programación de Windows de 64 bits
description: Microsoft ha lanzado versiones de 64 bits del sistema operativo Windows.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, Página principal
- Guía de programación para Windows de 64 bits Windows 64 bits programación de Windows consulte la guía de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1fa906510d3d9909c5cf888b562deaccb3496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418799"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guía de programación de Windows de 64 bits

Microsoft ha lanzado versiones de 64 bits del sistema operativo Windows. Windows de 64 bits se diseñó pensando en la compatibilidad. Los desarrolladores pueden garantizar que las aplicaciones de 32 bits existentes se ejecuten bien en Windows de 64 bits o aprovechar las ventajas de las ventanas de 64 bits mediante la migración de sus aplicaciones.

## <a name="benefits-of-64-bit-windows"></a>Ventajas de Windows de 64 bits

Un sistema operativo de 64 bits admite mucho más memoria física que un sistema operativo de 32 bits. Por ejemplo, la mayoría de los sistemas Windows de 32 bits admiten un máximo de 4 gigabytes de memoria física, con hasta 3 gigabytes de espacio de direcciones para cada proceso, mientras que Windows de 64 bits admite hasta 2 terabytes de memoria física con 8 terabytes de espacio de direcciones para cada proceso. El aumento de la memoria física incluye las siguientes ventajas para las aplicaciones:

-   Cada aplicación puede admitir más usuarios. Se debe replicar todo o parte de cada aplicación para cada usuario, lo que requiere memoria adicional.
-   Cada aplicación tiene un mejor rendimiento. La mayor cantidad de memoria física permite que se ejecuten más aplicaciones simultáneamente y que permanecen completamente residentes en la memoria principal del sistema. Esto reduce o elimina la reducción del rendimiento del intercambio de páginas a y desde el disco.
-   Cada aplicación tiene más memoria para el almacenamiento y la manipulación de datos. Las bases de datos pueden almacenar más datos en la memoria física del sistema. El acceso a los datos es más rápido porque no es necesario realizar lecturas de disco.
-   Las aplicaciones pueden manipular grandes cantidades de datos de forma fácil y confiable. La composición de vídeo para el trabajo de imagen de movimiento requiere Windows de 64 bits por este motivo. El modelado de aplicaciones científicas y financieras se beneficia en gran medida de las estructuras de datos residentes en memoria que no son posibles en Windows de 32 bits.

También hay importantes ventajas para las empresas:

-   Mayor productividad. Los trabajadores del conocimiento pueden dedicar su tiempo al pensamiento y la producción, en lugar de esperar a que el software finalice sus tareas.
-   Menor costo de propiedad. Cada servidor puede admitir un número mayor de usuarios y aplicaciones, por lo que su empresa necesitará menos servidores. Esto se traduce directamente en menos sobrecarga de administración, uno de los mayores costos en cualquier entorno informático.
-   Nuevas oportunidades de aplicación. Las nuevas aplicaciones se pueden diseñar sin las barreras impuestas por Windows de 32 bits. Las nuevas aplicaciones de gráficos harán que el trabajo sea más fácil y más agradable. Las tareas con un uso intensivo de datos que son imposibles hoy en día se pueden realizar con Windows de 64 bits.

## <a name="in-this-section"></a>En esta sección

-   [Preparación para Windows de 64 bits](getting-ready-for-64-bit-windows.md)
-   [Diseño de interfaces compatibles con 64 bits](designing-64-bit-compatible-interfaces.md)
-   [Ejecutar aplicaciones de 32 bits](running-32-bit-applications.md)
-   [Sugerencias de migración](migration-tips.md)

 

 




