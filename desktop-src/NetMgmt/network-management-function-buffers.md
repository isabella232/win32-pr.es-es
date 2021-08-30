---
title: Búferes de funciones de administración de red
description: La biblioteca en tiempo de ejecución rpc controla los búferes requeridos por las funciones de administración de red de recuperación de datos de 32 bits como se muestra a continuación.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8aba6a9ea2a3f01c7b70c86a31fc3a2e95801ac81f59688b1942ff2158c0045
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911685"
---
# <a name="network-management-function-buffers"></a>Búferes de funciones de administración de red

La biblioteca en tiempo de ejecución rpc controla los búferes requeridos por las funciones de administración de red de recuperación de datos de 32 bits de la siguiente manera:

-   **Enviar datos al servidor** (datos especificados por \[ en \] parámetros).

    El autor de la llamada debe asignar y desasignar el búfer para la estructura de información pertinente (o estructuras) y pasar una variable de puntero a la función. El autor de la llamada no necesita especificar la longitud del búfer.

    Ejemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Recuperar datos del servidor** (datos especificados por parámetros \[ \] out).

    El sistema asigna el búfer para la información devuelta. El autor de la llamada debe pasar una variable de puntero a la función en la entrada. Si la devolución es correcta, el puntero recibe la dirección del búfer asignado por el sistema que contiene la información devuelta. Esto simplifica el código de llamada, ya que el autor de la llamada no necesita calcular el tamaño del búfer ni cambiar el tamaño del búfer y volver a emitir la función.

    Cuando el autor de la llamada haya terminado de procesar la información devuelta, debe liberar la memoria asignada por el sistema mediante una llamada a la [**función NetApiBufferFree.**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) Para obtener más información sobre cómo especificar tamaños de búfer, vea [Longitudes de](network-management-function-buffer-lengths.md)búfer de la función de administración de redes .

    Ejemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




