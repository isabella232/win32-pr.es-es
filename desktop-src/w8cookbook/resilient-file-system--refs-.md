---
title: Sistema de archivos resistente
description: Sistema de archivos resistente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2938f99e232f37d6f36f575c6c2a419adf3b6dbdc2a06bd9c8e243d6ba4884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882685"
---
# <a name="resilient-file-system"></a>Sistema de archivos resistente

## <a name="platform"></a>Plataforma

**Servidores:** Windows Server 2012 

## <a name="description"></a>Descripción

El sistema de archivos resistente (ReFS) es un nuevo sistema de archivos local. Maximiza la disponibilidad de los datos, a pesar de los errores que históricamente provocarían la pérdida de datos o el tiempo de inactividad. La integridad de los datos garantiza que los datos críticos para la empresa estén protegidos frente a errores y estén disponibles cuando sea necesario. Su arquitectura está diseñada para proporcionar escalabilidad y rendimiento en una era de tamaños de conjunto de datos en constante crecimiento y cargas de trabajo dinámicas.

Las características clave de ReFS son:

-   **Integridad:** ReFS almacena los datos para que estén protegidos frente a muchos de los errores comunes que pueden provocar la pérdida de datos. Los metadatos del sistema de archivos siempre están protegidos. Opcionalmente, los datos de usuario se pueden proteger por volumen, por directorio o por archivo. Si se produce un daño, ReFS puede detectar y, cuando se configura con Espacios de almacenamiento, corregir automáticamente los daños. En caso de error del sistema, ReFS está diseñado para recuperarse de ese error rápidamente, sin pérdida de datos de usuario.
-   **Disponibilidad:** ReFS está diseñado para priorizar la disponibilidad de los datos. Con ReFS, si se producen daños y no se pueden reparar automáticamente, el proceso de recuperación en línea se localiza en el área de daños, sin necesidad de tiempo de incoación del volumen. En resumen, si se producen daños, ReFS permanecerá en línea.
-   **Escalabilidad:** ReFS está diseñado para los tamaños de conjunto de datos de hoy y los tamaños del conjunto de datos de mañana; está optimizado para una alta escalabilidad.
-   **Compatibilidad de** aplicaciones: para maximizar AppCompat, ReFS admite un subconjunto de características NTFS más las API de Win32 que se han adoptado ampliamente.
-   **Identificación** proactiva de errores: las funcionalidades de integridad de ReFS se aprovechan mediante un escáner de integridad de datos (un "depurador") que examina periódicamente el volumen, intenta identificar daños latentes y, a continuación, desencadena proactivamente una reparación de los datos dañados.

## <a name="resources"></a>Recursos

-   [Publicación Windows 8 blog: Creación del sistema de archivos de próxima generación para Windows: ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilidad de aplicaciones y ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 