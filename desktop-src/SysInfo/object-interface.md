---
description: 'Windows proporciona funciones que realizan las siguientes tareas:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interfaz de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3db15a60d88b8258f5959d2bf4cf447496cbe97ae906bdf087fe316f449b276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763994"
---
# <a name="object-interface"></a>Interfaz de objeto

Windows proporciona funciones que realizan las siguientes tareas:

-   Creación de un objeto
-   Obtener un identificador de objeto
-   Obtener información sobre el objeto
-   Establecer información sobre el objeto
-   Cierre el identificador de objeto
-   Destruir el objeto

Algunas de estas tareas no son necesarias para cada objeto. Algunas de estas tareas se combinan para determinados objetos. Por ejemplo, una aplicación puede crear un objeto de evento. Otras aplicaciones pueden abrir el evento para obtener un identificador único para este objeto de evento. A medida que cada aplicación termina de usar el evento , cierra su identificador al objeto . Cuando no hay ningún identificador abierto restante en el objeto de evento, el sistema destruye el objeto de evento. Por el contrario, una aplicación puede obtener un identificador para un objeto de ventana existente. Cuando el objeto de ventana ya no es necesario, la aplicación debe destruir el objeto , lo que invalida el identificador de ventana.

En ocasiones, un objeto permanece en memoria después de cerrar todos los identificadores de objeto. Por ejemplo, un subproceso podría crear un objeto de evento y esperar en el identificador de evento. Mientras el subproceso está esperando, otro subproceso podría cerrar el mismo identificador de objeto de evento. El objeto de evento permanece en memoria, sin ningún identificador de objeto de evento, hasta que el objeto de evento se establece en el estado señalado y se completa la operación de espera. En este momento, el sistema quita el objeto de la memoria.

Los identificadores y objetos consumen memoria. Por lo tanto, para conservar el rendimiento del sistema, debe cerrar los identificadores y eliminar objetos en cuanto ya no sean necesarios. Si no lo hace, la aplicación puede dañar el rendimiento del sistema debido al uso excesivo del archivo de paginación.

Cuando finaliza un proceso, el sistema cierra automáticamente los identificadores y elimina los objetos creados por el proceso. Sin embargo, cuando un subproceso finaliza, el sistema normalmente no cierra identificadores ni elimina objetos. Las únicas excepciones son objetos de conversación de ventana, enlace, posición de ventana e intercambio dinámico de datos (DDE); Estos objetos se destruyen cuando finaliza el subproceso de creación.

 

 



