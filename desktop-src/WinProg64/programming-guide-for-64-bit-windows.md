---
title: Guía de programación de Windows de 64 bits
description: Microsoft ha publicado versiones de 64 bits del Windows operativo.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guía de programación de 64 Windows de programación de 64 Windows bits
- Guía de programación de 64 Windows de programación de 64 Windows, página principal
- Guía de programación para programación de 64 Windows programación de 64 Windows de 64 bits Consulte guía de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743472"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guía de programación de Windows de 64 bits

Microsoft ha publicado versiones de 64 bits del Windows operativo. El Windows de 64 bits se diseñó pensando en la compatibilidad. Los desarrolladores pueden asegurarse de que sus aplicaciones de 32 bits existentes se ejecutan bien en Windows de 64 bits o aprovechar las ventajas de las aplicaciones de 64 Windows mediante la migración de sus aplicaciones.

## <a name="benefits-of-64-bit-windows"></a>Ventajas de la conexión de 64 bits Windows

Un sistema operativo de 64 bits admite mucho más memoria física que un sistema operativo de 32 bits. Por ejemplo, la mayoría de los sistemas Windows de 32 bits admiten un máximo de 4 gigabytes de memoria física, con hasta 3 gigabytes de espacio de direcciones para cada proceso, mientras que el Windows de 64 bits admite hasta 2 terabytes de memoria física con 8 terabytes de espacio de direcciones para cada proceso. El aumento de la memoria física incluye las siguientes ventajas para las aplicaciones:

-   Cada aplicación puede admitir más usuarios. Todos o parte de cada aplicación se deben replicar para cada usuario, lo que requiere memoria adicional.
-   Cada aplicación tiene un mejor rendimiento. El aumento de la memoria física permite que más aplicaciones se ejecuten simultáneamente y permanezcan completamente residentes en la memoria principal del sistema. Esto reduce o elimina la reducción del rendimiento del intercambio de páginas hacia y desde el disco.
-   Cada aplicación tiene más memoria para el almacenamiento y la manipulación de datos. Las bases de datos pueden almacenar más datos en la memoria física del sistema. El acceso a los datos es más rápido porque las lecturas de disco no son necesarias.
-   Las aplicaciones pueden manipular grandes cantidades de datos de forma fácil y confiable. La composición de vídeo para el trabajo de imagen de movimiento requiere 64 bits Windows por este motivo. El modelado de aplicaciones científicas y financieras se beneficia en gran medida de las estructuras de datos residentes en memoria que no son posibles en aplicaciones de 32 Windows.

También hay ventajas importantes para las empresas:

-   Mayor productividad. Los trabajadores del conocimiento pueden dedicar su tiempo a pensar y producir, en lugar de esperar a que el software finalice sus tareas.
-   Menor costo de propiedad. Cada servidor puede admitir un mayor número de usuarios y aplicaciones, por lo que su empresa necesitará menos servidores. Esto se traduce directamente en menos sobrecarga de administración, uno de los mayores costos en cualquier entorno informático.
-   Nuevas oportunidades de aplicación. Las nuevas aplicaciones se pueden diseñar sin las barreras impuestas por las aplicaciones de 32 Windows. Las nuevas aplicaciones gráficas harán que el trabajo sea más fácil y divertido. Las tareas de uso intensivo de datos que hoy en día son imposibles se pueden realizar con tareas de 64 Windows.

## <a name="in-this-section"></a>En esta sección

-   [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md)
-   [Diseño de interfaces compatibles de 64 bits](designing-64-bit-compatible-interfaces.md)
-   [Ejecución de aplicaciones de 32 bits](running-32-bit-applications.md)
-   [Sugerencias de migración](migration-tips.md)

 

 




