---
title: Administración de conjuntos de conexiones de red (asociaciones)
description: A partir de Windows 2000, el tiempo de ejecución de RPC puede mantener más de una conexión entre el cliente y el servidor.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Administración de conjuntos de conexiones de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e99afe23d90e44d85dc7a2ec9301b45e1f20b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269130"
---
# <a name="managing-network-connection-sets-associations"></a>Administración de conjuntos de conexiones de red (asociaciones)

A partir de Windows 2000, el tiempo de ejecución de RPC puede mantener más de una conexión entre el cliente y el servidor. Esto facilita la operación en los transportes que no admiten el cambio de la identidad del cliente sin tener que volver a establecer la conexión, los clientes multiproceso y los clientes asincrónicos. El conjunto de conexiones entre un proceso de cliente y un punto de conexión de servidor se denomina *Asociación* en la terminología de RPC. Comprender las asociaciones puede mejorar la implementación de RPC.

En un escenario de identidad de un solo subproceso y de un solo cliente, RPC abre una conexión entre un proceso de cliente y un punto de conexión de servidor para realizar llamadas RPC. Cuando se realiza una llamada RPC sincrónica, el cliente envía la solicitud al servidor en esta conexión y recibe también la respuesta. Cuando crece el número de subprocesos que realizan llamadas RPC en el proceso del cliente, la identidad de seguridad del cliente puede cambiar. Cuando se mezclan llamadas asincrónicas/canalizaciones con llamadas sincrónicas en el cliente, RPC puede necesitar más de una conexión de red. Todas las conexiones del conjunto se colocan en un grupo de conexiones denominado Asociación.

Una llamada a procedimiento remoto sincrónico utiliza exclusivamente una conexión determinada para cumplir con los estándares de RPC. Una conexión utilizada por una llamada RPC sincrónica se considera ocupada si se ha enviado una solicitud, pero no se ha recibido una respuesta. No se permite ningún otro tráfico en esa conexión hasta que se reciba la respuesta. El tiempo de ejecución de RPC intenta multiplexar llamadas RPC asincrónicas y de canalización en la misma conexión. No se pueden mezclar llamadas sincrónicas y asincrónicas/canalizaciones en la misma conexión, lo que significa que se puede usar una conexión determinada para llamadas RPC sincrónicas o para llamadas RPC asincrónicas o de canalización.

RPC intenta de forma agresiva volver a usar las conexiones del grupo. Cuando se realiza una nueva llamada RPC, RPC intenta encontrar una conexión adecuada del grupo y crea una nueva conexión solo si no se encuentra una conexión adecuada. Para que una conexión se considere adecuada, debe:

-   Ser del tipo adecuado (sincrónico o asincrónico/canalización).
-   Sea gratuito.
-   Tienen la misma identidad de seguridad que el controlador de enlace en el que se realiza la llamada. Si se utiliza el seguimiento de identidad dinámica, la identidad del identificador de enlace se actualiza desde el token del subproceso al principio de la llamada. Si se utiliza el seguimiento de identidad estático, se usa la identidad del cliente marcada en el identificador de enlace.

Cuando se completa la llamada, una vez recibida la respuesta, la conexión se marca como gratuita y se puede usar para otras llamadas RPC.

No se puede cambiar la identidad de seguridad en una conexión. Por ejemplo, si se realiza un gran número de llamadas al mismo servidor en identidades de seguridad diferentes, el número de conexiones en el grupo de subprocesos crece. La propia asociación se cuenta como referencia y, cuando todas las referencias han desaparecido, detiene y cierra todas las conexiones. Cada identificador de enlace y cada identificador de contexto contienen una referencia en la asociación. Cuando se cierra todo, la Asociación desaparece. En Windows XP, las asociaciones no desaparecen necesariamente inmediatamente; pueden permanecer durante un breve período (el período de destino es de 20 segundos, pero el tiempo de ejecución de RPC puede optar por retrasar la destrucción de la asociación si no hay ningún subproceso disponible para ejecutar la tarea). Si no desea que la Asociación permanezca activa después de que se cierre el último identificador de contexto o identificador de enlace, use la opción no persistente de RPC \_ C \_ \_ \_ para forzar al tiempo de ejecución de RPC a cerrar inmediatamente la conexión.

 

 




