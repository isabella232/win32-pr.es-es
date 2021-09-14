---
description: Puede minimizar el impacto que la aplicación tiene en otros clientes y el impacto que tienen en la aplicación al conceder tanto uso compartido como sea posible, solicitar el nivel de acceso mínimo necesario y usar el bloqueo oportunista menos intrusivo adecuado para la aplicación.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Respuesta del servidor a solicitudes abiertas en archivos bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069846"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Respuesta del servidor a solicitudes abiertas en archivos bloqueados

La vida de un bloqueo oportunista incluye tres intervalos de tiempo distintos. Durante cada una, el servidor determina por distintos medios su reacción a una solicitud de un cliente para abrir un archivo bloqueado por otro cliente. En general, puede minimizar el impacto que la aplicación tiene en otros clientes y el impacto que tienen en la aplicación al conceder tanto uso compartido como sea posible, solicitar el nivel de acceso mínimo necesario y usar el bloqueo oportunista menos intrusivo adecuado para la aplicación.

En primer lugar, es el período después de que el servidor abra un archivo para un cliente, pero antes de conceder un bloqueo. Durante este tiempo, no existe ningún bloqueo en el archivo y el servidor depende del uso compartido, los modos de acceso y el tipo de bloqueo oportunista que solicite para determinar su reacción a otra solicitud para abrir el mismo archivo. Por ejemplo, si abre el archivo en cuestión para el acceso de escritura, puede impedir la concesión de bloqueos oportunistas que permitan el acceso de almacenamiento en caché de lectura a otros clientes. El intervalo de tiempo antes de que el servidor conceda un bloqueo suele estar en el intervalo de milisegundos, pero puede ser más largo.

Una vez concedido el bloqueo oportunista, el servidor examina el bloqueo para determinar la reacción del servidor a una solicitud abierta en un archivo bloqueado. Una vez más, la forma en que la aplicación abrió el archivo y el tipo de bloqueo que contiene afecta a cómo responde el servidor. Para obtener más información sobre cómo responde el servidor en cada caso, vea [Tipos de bloqueos oportunistas.](types-of-opportunistic-locks.md)

Por último, existe el intervalo después de que el servidor determine que el bloqueo se debe interrumpir (finalizar), pero antes de que la aplicación complete su reacción a la interrupción. Según el tipo de bloqueo, la aplicación puede degradar el bloqueo a un nivel inferior o a ninguno en absoluto. La aplicación también puede cerrar el archivo y el bloqueo. Durante este tiempo, el servidor mantiene en espera las solicitudes de otros clientes para abrir el archivo bloqueado anteriormente. Este intervalo de tiempo puede oscilar entre milisegundos y decenas de segundos. Para obtener más información, [vea Breaking Opportunistic Locks](breaking-opportunistic-locks.md).

 

 



