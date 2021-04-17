---
description: 'Windows proporciona funciones que realizan las siguientes tareas:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interfaz de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497687"
---
# <a name="object-interface"></a>Interfaz de objeto

Windows proporciona funciones que realizan las siguientes tareas:

-   Creación de un objeto
-   Obtener un identificador de objeto
-   Obtener información sobre el objeto
-   Establecer información sobre el objeto
-   Cerrar el identificador de objeto
-   Destruir el objeto

Algunas de estas tareas no son necesarias para cada objeto. Algunas de estas tareas se combinan para determinados objetos. Por ejemplo, una aplicación puede crear un objeto de evento. Otras aplicaciones pueden abrir el evento para obtener un identificador único de este objeto de evento. A medida que cada aplicación termina de usar el evento, cierra su identificador al objeto. Cuando no quedan identificadores abiertos en el objeto de evento, el sistema destruye el objeto de evento. En cambio, una aplicación puede obtener un identificador de un objeto de ventana existente. Cuando el objeto de ventana ya no se necesita, la aplicación debe destruir el objeto, lo que invalida el identificador de la ventana.

En ocasiones, un objeto permanece en memoria una vez cerrados todos los identificadores de objeto. Por ejemplo, un subproceso podría crear un objeto de evento y esperar en el controlador de eventos. Mientras el subproceso está esperando, otro subproceso podría cerrar el mismo identificador de objeto de evento. El objeto de evento permanece en memoria, sin identificadores de objeto de evento, hasta que el objeto de evento se establece en el estado señalado y se completa la operación de espera. En este momento, el sistema quita el objeto de la memoria.

Los identificadores y los objetos consumen memoria. Por lo tanto, para mantener el rendimiento del sistema, debe cerrar los identificadores y eliminar objetos en cuanto ya no se necesiten. Si no lo hace, la aplicación puede perjudicar el rendimiento del sistema, debido al uso excesivo del archivo de paginación.

Cuando finaliza un proceso, el sistema cierra automáticamente los identificadores y elimina los objetos creados por el proceso. Sin embargo, cuando un subproceso finaliza, el sistema normalmente no cierra los identificadores ni los objetos de eliminación. Las únicas excepciones son los objetos de la ventana, el enlace, la posición de la ventana y el intercambio dinámico de datos (DDE). Estos objetos se destruyen cuando finaliza el subproceso de creación.

 

 



