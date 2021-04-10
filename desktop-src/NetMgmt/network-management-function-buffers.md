---
title: Búferes de función de administración de red
description: La biblioteca en tiempo de ejecución de RPC controla los búferes que requieren las funciones de administración de red de recuperación de datos de 32 bits como se indica a continuación.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268917"
---
# <a name="network-management-function-buffers"></a>Búferes de función de administración de red

La biblioteca en tiempo de ejecución de RPC controla los búferes que requieren las funciones de administración de red de recuperación de datos de 32 bits de la siguiente manera:

-   **Enviar datos al servidor** (datos especificados por \[ \] los parámetros in).

    El autor de la llamada debe asignar y desasignar el búfer de la estructura (o estructuras) de información pertinente y pasar una variable de puntero a la función. El autor de la llamada no necesita especificar la longitud del búfer.

    Ejemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Recuperar datos del servidor** (datos especificados por \[ parámetros out \] ).

    El sistema asigna el búfer para la información devuelta. El llamador debe pasar una variable de puntero a la función en la entrada. El puntero recibe la dirección del búfer asignado por el sistema que contiene la información devuelta, si la devolución es correcta. Esto simplifica el código de llamada, porque el autor de la llamada no necesita calcular el tamaño del búfer o cambiar el tamaño del búfer y volver a emitir la función.

    Cuando el autor de la llamada ha terminado de procesar la información devuelta, debe liberar la memoria asignada por el sistema mediante una llamada a la función [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) . Para obtener más información sobre cómo especificar los tamaños de búfer, vea [longitud de búfer de funciones de administración de red](network-management-function-buffer-lengths.md).

    Ejemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




