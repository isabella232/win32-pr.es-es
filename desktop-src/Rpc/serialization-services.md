---
title: Servicios de serialización
description: Rpc de Microsoft admite dos métodos para codificar y codificar datos, denominados colectivamente serialización de datos.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Llamada a procedimiento remoto RPC, descrita, serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473540"
---
# <a name="serialization-services"></a>Servicios de serialización

Rpc de Microsoft admite dos métodos para codificar y codificar datos, denominados colectivamente *serialización de datos*. La serialización significa que los datos se serializan en los búferes que se controlan y se desmarcieron de estos. Esto difiere del uso tradicional de RPC, en el que los códigos auxiliares y la biblioteca en tiempo de ejecución de RPC tienen control total de los búferes de serialización y el proceso es transparente. Puede usar el búfer para el almacenamiento en medios permanentes, cifrado, y así sucesivamente. Al codificar los datos, los códigos auxiliares rpc serializan los datos en un búfer y le pasan el búfer. Al descodificar datos, se proporciona un búfer de serialización con datos en él y los datos se desmarcó del búfer a la memoria. Puede serializar por procedimiento o tipo.

> [!Note]  
> El término *pickling se* usa normalmente entre los desarrolladores para describir la serialización. De hecho, los ejemplos Windows SDK contienen un directorio denominado *pickle* que conserva los programas de ejemplo de serialización RPC.

 

La serialización aprovecha los mecanismos RPC para serializar y desmarque de datos para otros fines. Por ejemplo, en lugar de usar varias operaciones de E/S para serializar un grupo de objetos en una secuencia, una aplicación puede optimizar el rendimiento serializando varios objetos de tipos diferentes en un búfer y, a continuación, escribiendo todo el búfer en una sola operación. Las funciones que manipulan los identificadores de serialización son independientes del tipo de serialización que se usa.

Como otro ejemplo, si necesita usar un mecanismo de transporte de red además de RPC, como Microsoft Windows Sockets (Winsock). Con la serialización RPC, el programa puede realizar llamadas a funciones que serializan los datos en búferes y, a continuación, transmitir estos datos mediante Winsock. Cuando la aplicación recibe datos, puede usar el mecanismo de serialización RPC para desmarque los datos de los búferes rellenados por las rutinas winsock. Esto proporciona muchas de las ventajas de las aplicaciones de estilo RPC y, al mismo tiempo, permite usar mecanismos de transporte que no son RPC.

También puede usar la serialización para fines no relacionados con las comunicaciones de red. Por ejemplo, una vez que use las funciones de codificación RPC para serializar los datos en un búfer, puede almacenarlo en un archivo para que lo use otra aplicación. También puede cifrarlo. Incluso puede usarlo para almacenar una representación independiente del hardware y del sistema operativo de los datos en una base de datos.

En los temas siguientes se presenta una explicación de los servicios de serialización que admite Microsoft RPC:

-   [Uso de servicios de serialización](using-serialization-services.md)
-   [Serialización de procedimientos](procedure-serialization.md)
-   [Serialización de tipos](type-serialization.md)
-   [Identificadores de serialización](serialization-handles.md)

 

 




