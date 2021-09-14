---
description: El Monitor de red binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Monitor de red blobs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245330"
---
# <a name="network-monitor-blobs"></a>Monitor de red blobs

El Monitor de red binario grande (BLOB) es una estructura de datos genérica que contiene información de configuración y ubicación de tarjetas de interfaz de red (NIC). Use blobs para representar NIC y filtrar entradas en una lista de NIC. Los BLOBS también pueden contener datos específicos de la aplicación sin afectar a los demás datos que contienen. La implementación de BLOB es opaca para todos los niveles que deben tener acceso a blobs con las API de BLOB.

## <a name="blob-structure"></a>Estructura BLOB

Un BLOB se puede considerar como un árbol jerárquico que se usa para designar cadenas. Este árbol tiene tres capas: Propietario, Categoría y Etiqueta. Propietario es una cadena que indica, en general, quién lee una entrada. La categoría también es una cadena, que designa una agrupación funcional general de etiquetas bajo el propietario. La etiqueta es el nombre real de la entrada.

Las características estructurales de los blobs incluyen:

-   Los asistentes de BLOB dentro de un proceso están protegidos entre sí mediante una exclusión mutua integrada en cada BLOB.
-   Cada BLOB tiene un número de versión interno para que los asistentes puedan controlar los formularios BLOB presentes y futuros. Pueden producirse conflictos de versión si envía un BLOB a otro equipo a través de una llamada a procedimiento remoto.
-   El propio BLOB es un puntero a un void. Tenga en cuenta que las aplicaciones deben asignar blobs con el modificador **const** para evitar modificar el contenido.
-   Cada uno de los designadores, así como sus valores, son cadenas. Tenga en cuenta que las cadenas devueltas por las **funciones GetString** son realmente punteros al BLOB y no se deben cambiar. Por esta razón, estas cadenas deben especificarse como **const char** _ pX* para evitar que las \_ aplicaciones cambien accidentalmente.

En general, todos los parámetros con el **designador const** animan al autor de la llamada a no cambiar los valores en lugar de prohibir que las funciones auxiliares los cambien. De hecho, las funciones auxiliares normalmente cambiarán esos valores.

 

 



