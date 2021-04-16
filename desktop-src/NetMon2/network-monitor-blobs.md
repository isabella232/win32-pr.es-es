---
description: El Monitor de red objeto binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Blobs Monitor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689560"
---
# <a name="network-monitor-blobs"></a>Blobs Monitor de red

El Monitor de red objeto binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC). Use blobs para representar NIC y filtrar entradas en una lista de NIC. Los blobs también pueden contener datos específicos de la aplicación sin que ello afecte a los demás datos que contienen. La implementación de BLOB es opaca para todos los niveles que deben tener acceso a los blobs con las API de BLOB.

## <a name="blob-structure"></a>Estructura de BLOB

Un BLOB se puede considerar como un árbol jerárquico que se usa para designar cadenas. Este árbol tiene tres niveles: propietario, categoría y etiqueta. Owner es una cadena que indica, en general, quién lee una entrada. La categoría también es una cadena, que designa una agrupación funcional general de etiquetas bajo el propietario. La etiqueta es el nombre real de la entrada.

Las características estructurales de los blobs incluyen:

-   Las aplicaciones auxiliares de BLOB dentro de un proceso están protegidas entre sí mediante una exclusión mutua integrada en cada BLOB.
-   Cada BLOB tiene un número de versión interno para que las aplicaciones auxiliares puedan administrar formularios de BLOB presentes y futuros. Pueden producirse conflictos de versión si envía un BLOB a otro equipo a través de una llamada a procedimiento remoto.
-   El propio BLOB es un puntero a un void. Tenga en cuenta que las aplicaciones deben asignar blobs con el modificador **const** para evitar modificar el contenido.
-   Cada uno de los designadores, así como sus valores, son cadenas. Tenga en cuenta que las cadenas devueltas por las funciones **GetString** son realmente punteros en el BLOB y no se deben cambiar. Por este motivo, estas cadenas se deben especificar como **const char** _ \_ PX * para evitar que las aplicaciones las cambien accidentalmente.

En general, todos los parámetros con el designador **const** animan al autor de la llamada a abstenerse de cambiar los valores en lugar de impedir que las funciones auxiliares las cambien. De hecho, las funciones auxiliares normalmente cambiarán esos valores.

 

 



