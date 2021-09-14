---
title: Búferes de función de administración de redes
description: La biblioteca rpc en tiempo de ejecución controla los búferes requeridos por las funciones de administración de red de recuperación de datos de 32 bits como se muestra a continuación.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245426"
---
# <a name="network-management-function-buffers"></a>Búferes de función de administración de redes

La biblioteca rpc en tiempo de ejecución controla los búferes requeridos por las funciones de administración de red de recuperación de datos de 32 bits como se muestra a continuación:

-   **Envío de datos al servidor** (datos especificados por en \[ \] parámetros).

    El autor de la llamada debe asignar y desasignar el búfer para la estructura de información pertinente (o estructuras) y pasar una variable de puntero a la función. El autor de la llamada no necesita especificar la longitud del búfer.

    Ejemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Recuperar datos del servidor** (datos especificados por parámetros \[ \] out).

    El sistema asigna el búfer para la información devuelta. El autor de la llamada debe pasar una variable de puntero a la función en la entrada. Si la devolución es correcta, el puntero recibe la dirección del búfer asignado por el sistema que contiene la información devuelta. Esto simplifica el código de llamada, ya que el autor de la llamada no necesita calcular el tamaño del búfer ni cambiar el tamaño del búfer y volver a emitir la función.

    Cuando el autor de la llamada haya terminado de procesar la información devuelta, debe liberar la memoria asignada por el sistema llamando a la [**función NetApiBufferFree.**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) Para obtener más información sobre cómo especificar tamaños de búfer, vea [Longitudes de](network-management-function-buffer-lengths.md)búfer de la función de administración de redes .

    Ejemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




