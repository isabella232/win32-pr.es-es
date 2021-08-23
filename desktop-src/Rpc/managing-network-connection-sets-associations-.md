---
title: Administración de conjuntos de conexiones de red (asociaciones)
description: A partir Windows 2000, el tiempo de ejecución rpc puede mantener más de una conexión entre el cliente y el servidor.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Administración de conjuntos de conexiones de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def88053639c2911dca26d57a080c7fbcbd71728000bee2f12ca7440cb56320b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928391"
---
# <a name="managing-network-connection-sets-associations"></a>Administración de conjuntos de conexiones de red (asociaciones)

A partir Windows 2000, el tiempo de ejecución rpc puede mantener más de una conexión entre el cliente y el servidor. Esto facilita el funcionamiento en transportes que no admiten el cambio de la identidad del cliente sin restablecer la conexión, los clientes multiproceso y los clientes asincrónicos. El conjunto de conexiones entre un proceso de cliente y un punto de conexión de servidor se denomina *asociación en* terminología RPC. Comprender las asociaciones puede mejorar la implementación de RPC.

En un escenario de identidad de cliente único de un solo subproceso, RPC abre una conexión entre un proceso de cliente y un punto de conexión de servidor para realizar llamadas RPC. Cuando se realiza una llamada RPC sincrónica, el cliente envía la solicitud al servidor en esta conexión y recibe también la respuesta en ella. Cuando aumenta el número de subprocesos que hacen llamadas RPC en el proceso de cliente, la identidad de seguridad del cliente puede cambiar. Cuando las llamadas asincrónicas o de canalización se mezclan con llamadas sincrónicas en el cliente, RPC puede necesitar más de una conexión de red. Todas las conexiones del conjunto se ponen en un grupo de conexiones denominado asociación.

Una llamada a procedimiento remoto sincrónico usa exclusivamente una conexión determinada para cumplir con los estándares RPC. Una conexión usada por una llamada RPC sincrónica se considera ocupada si se ha enviado una solicitud, pero no se ha recibido una respuesta. No se permite ningún otro tráfico en esa conexión hasta que se recibe la respuesta. El tiempo de ejecución de RPC intenta multiplexizar llamadas RPC asincrónicas y canalizar en la misma conexión. Las llamadas sincrónicas y asincrónicas o de canalización no se pueden mezclar en la misma conexión, lo que significa que se puede usar una conexión determinada para llamadas RPC sincrónicas o para llamadas RPC asincrónicas o de canalización.

RPC intenta volver a usar las conexiones del grupo de forma agresiva. Cuando se realiza una nueva llamada RPC, RPC intenta encontrar una conexión adecuada desde el grupo y crea una nueva conexión solo si no se encuentra una conexión adecuada. Para que una conexión se considere adecuada, debe:

-   Ser del tipo adecuado (sincrónico o asincrónico/canalización).
-   Ser gratis.
-   Tenga la misma identidad de seguridad que el identificador de enlace en el que se realiza la llamada. Si se usa el seguimiento dinámico de identidades, la identidad del identificador de enlace se actualiza desde el token de subproceso al principio de la llamada. Si se usa el seguimiento de identidades estático, se usa la identidad de cliente con la marca en el identificador de enlace.

Una vez completada la llamada, una vez recibida la respuesta, la conexión se marca como libre y se puede usar para otras llamadas RPC.

La identidad de seguridad de una conexión no puede cambiar. Por ejemplo, si un gran número de llamadas al mismo servidor se realizan en identidades de seguridad diferentes, aumenta el número de conexiones del grupo de subprocesos. La propia asociación cuenta las referencias y, cuando todas las referencias han desaparecido, se detiene y cierra todas las conexiones. Cada identificador de enlace y cada identificador de contexto tienen una referencia sobre la asociación. Cuando se cierran todas, la asociación desaparece. En Windows XP, las asociaciones no desaparecen necesariamente inmediatamente; pueden permanecer durante un breve período (el período de destino es de 20 segundos, pero el tiempo de ejecución rpc puede retrasar la destrucción de la asociación si no hay subprocesos disponibles para ejecutar la tarea). Si no desea que la asociación permanezca activa después de cerrar el último identificador de contexto o de enlace, use la opción RPC \_ C \_ OPT \_ DONT LINGER para forzar que rpc Runtime cierre inmediatamente la \_ conexión.

 

 




