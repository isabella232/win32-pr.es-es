---
description: Puede minimizar el impacto que tiene la aplicación en otros clientes y el impacto que tienen en la aplicación al conceder tantos recursos compartidos como sea posible, solicitar el nivel de acceso mínimo necesario y usar el menos bloqueo oportunista intrusivo adecuado para su aplicación.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Respuesta del servidor para abrir solicitudes en archivos bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542502"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Respuesta del servidor para abrir solicitudes en archivos bloqueados

La duración de un bloqueo oportunista incluye tres intervalos de tiempo distintos. Durante cada una de ellas, el servidor determina por diferentes significa su reacción a una solicitud de un cliente para abrir un archivo bloqueado por otro cliente. En general, puede minimizar el impacto que tiene la aplicación en otros clientes y el impacto que tienen en la aplicación al conceder tantos recursos compartidos como sea posible, solicitar el nivel de acceso mínimo necesario y usar el menor bloqueo oportunista intrusivo adecuado para su aplicación.

El primero es el período después de que el servidor abra un archivo para un cliente, pero antes de conceder un bloqueo. Durante este tiempo, no hay ningún bloqueo en el archivo y el servidor depende del uso compartido, los modos de acceso y el tipo de bloqueo oportunista que solicita para determinar su reacción a otra solicitud para abrir el mismo archivo. Por ejemplo, si abre el archivo en cuestión para el acceso de escritura, puede impedir la concesión de bloqueos oportunistas que permitan el acceso al almacenamiento en caché de lectura a otros clientes. El intervalo de tiempo antes de que el servidor conceda un bloqueo normalmente está en el intervalo de milisegundos, pero puede ser más largo.

Una vez concedido el bloqueo oportunista, el servidor examina el bloqueo para determinar la reacción del servidor a una solicitud abierta en un archivo bloqueado. De nuevo, el modo en que la aplicación abrió el archivo y el tipo de bloqueo que contiene afecta a la respuesta del servidor. Para obtener más información sobre cómo responde el servidor en cada caso, consulte [tipos de bloqueos oportunistas](types-of-opportunistic-locks.md).

Por último, hay un intervalo después de que el servidor determine que el bloqueo se debe interrumpir (finaliza), pero antes de que la aplicación complete su reacción a la interrupción. Dependiendo del tipo de bloqueo, la aplicación puede degradar el bloqueo a un nivel inferior o a ninguno. La aplicación también puede cerrar el archivo y el bloqueo. Durante este tiempo, el servidor mantiene en abeyance cualquier solicitud de otros clientes para abrir el archivo previamente bloqueado. Este intervalo de tiempo puede oscilar entre milisegundos y decenas de segundos. Para obtener más información, vea [interrumpir bloqueos oportunistas](breaking-opportunistic-locks.md).

 

 



