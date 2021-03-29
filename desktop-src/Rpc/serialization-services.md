---
title: Servicios de serialización
description: Microsoft RPC admite dos métodos para codificar y descodificar datos, denominados colectivamente datos de serialización.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- RPC llamada a procedimiento remoto, descripción, serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779080"
---
# <a name="serialization-services"></a>Servicios de serialización

Microsoft RPC admite dos métodos para codificar y descodificar datos, denominados colectivamente *datos de serialización*. La serialización significa que se calculan las referencias de los datos y se calculan las referencias de los búferes que se controlan. Esto difiere del uso tradicional de RPC, en el que el código auxiliar y la biblioteca en tiempo de ejecución de RPC tienen control total de los búferes de serialización y el proceso es transparente. Puede usar el búfer para el almacenamiento en medios permanentes, cifrado, etc. Al codificar datos, el código auxiliar de RPC calcula las referencias de los datos en un búfer y le pasa el búfer. Al descodificar datos, se proporciona un búfer de serialización con datos en él y se anula la serialización de los datos del búfer en la memoria. Puede serializar a partir de un procedimiento o de un tipo.

> [!Note]  
> La *selección* del término se usa normalmente entre los desarrolladores para describir la serialización. De hecho, los ejemplos de Windows SDK contienen un directorio denominado *Pickle* que conserva los programas de ejemplo de serialización de RPC.

 

La serialización aprovecha los mecanismos RPC para calcular las referencias y calcular las referencias de los datos para otros propósitos. Por ejemplo, en lugar de usar varias operaciones de e/s para serializar un grupo de objetos en una secuencia, una aplicación puede optimizar el rendimiento al serializar varios objetos de tipos diferentes en un búfer y, a continuación, escribir todo el búfer en una sola operación. Las funciones que manipulan los identificadores de serialización son independientes del tipo de serialización que se está usando.

Otro ejemplo: Si necesita usar un mecanismo de transporte de red además de RPC, como Microsoft Windows Sockets (Winsock). Con la serialización de RPC, el programa puede realizar llamadas a funciones que serializan los datos en búferes y, a continuación, transmiten estos datos mediante Winsock. Cuando la aplicación recibe datos, puede utilizar el mecanismo de serialización de RPC para anular las referencias de los datos de los búferes rellenados por las rutinas Winsock. Esto proporciona muchas de las ventajas de las aplicaciones de estilo RPC y, al mismo tiempo, permite usar mecanismos de transporte que no son de RPC.

También puede usar la serialización para fines no relacionados con las comunicaciones de red. Por ejemplo, una vez que use las funciones de codificación RPC para calcular las referencias de los datos en un búfer, puede almacenarlos en un archivo para su uso por otra aplicación. También se puede cifrar. Incluso puede usarlo para almacenar una representación independiente del hardware y del sistema operativo de los datos en una base de datos de.

En los temas siguientes se presenta una descripción de los servicios de serialización que admite Microsoft RPC:

-   [Usar servicios de serialización](using-serialization-services.md)
-   [Serialización de procedimientos](procedure-serialization.md)
-   [Serialización de tipo](type-serialization.md)
-   [Identificadores de serialización](serialization-handles.md)

 

 




