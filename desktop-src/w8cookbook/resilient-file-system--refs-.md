---
title: Sistema de archivos resistente
description: Sistema de archivos resistente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104078547"
---
# <a name="resilient-file-system"></a>Sistema de archivos resistente

## <a name="platform"></a>Plataforma

**Servidores** : Windows Server 2012 

## <a name="description"></a>Descripción

El sistema de archivos resistente (ReFS) es un nuevo sistema de archivos local. Maximiza la disponibilidad de los datos, a pesar de los errores que históricamente podrían provocar la pérdida de datos o el tiempo de inactividad. La integridad de los datos garantiza que los datos críticos para la empresa estén protegidos frente a errores y estén disponibles cuando sea necesario. Su arquitectura está diseñada para proporcionar escalabilidad y rendimiento en una era de tamaños de conjunto de datos y cargas de trabajo dinámicas en constante crecimiento.

Las principales características de ReFS son:

-   **Integridad**: ReFS almacena datos para que estén protegidos frente a muchos de los errores comunes que pueden provocar la pérdida de datos. Los metadatos del sistema de archivos siempre están protegidos. Opcionalmente, los datos de usuario se pueden proteger por volumen, por directorio o por archivo. Si se producen daños, ReFS puede detectar y, cuando se configuran con espacios de almacenamiento, corregir automáticamente los daños. En caso de que se produzca un error del sistema, ReFS está diseñado para recuperarse rápidamente del error, sin pérdida de datos de usuario.
-   **Disponibilidad**: ReFS está diseñado para priorizar la disponibilidad de los datos. Con ReFS, si se producen daños y no puede repararse automáticamente, el proceso de recuperación en línea se localiza en el área de daños, por lo que no se requiere tiempo de inactividad del volumen. En Resumen, si se producen daños, ReFS permanecerá en línea.
-   **Escalabilidad**: ReFS está diseñado para los tamaños de los conjuntos de datos de hoy y los tamaños de los conjuntos de datos de mañana. está optimizado para una alta escalabilidad.
-   **Compatibilidad de aplicaciones**: para maximizar AppCompat, ReFS admite un subconjunto de características de NTFS más las API de Win32 que se han adoptado ampliamente.
-   **Identificación de errores proactivo**: las capacidades de integridad de ReFS las aprovecha un escáner de integridad de datos (un "limpiador") que examina periódicamente el volumen, intenta identificar daños latentes y, después, desencadena de forma proactiva una reparación de los datos dañados.

## <a name="resources"></a>Recursos

-   [Publicación de blog de Windows 8: compilar el sistema de archivos de la próxima generación para Windows: ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilidad de aplicaciones y ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 