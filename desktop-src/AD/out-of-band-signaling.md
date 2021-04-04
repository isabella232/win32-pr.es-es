---
title: Señalización fuera de banda
description: Las aplicaciones cooperativas que comparten datos comunes mediante el directorio pueden usar señales fuera de banda para evitar el sesgo de versiones y las actualizaciones parciales.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075111"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="cc2b7-103">Señalización fuera de banda</span><span class="sxs-lookup"><span data-stu-id="cc2b7-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="cc2b7-104">Las aplicaciones cooperativas que comparten datos comunes mediante el directorio pueden usar señales fuera de banda para evitar el sesgo de versiones y las actualizaciones parciales.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="cc2b7-105">En pocas palabras, las aplicaciones que cooperan usan un mecanismo independiente de la replicación de directorios para informar mutuamente de los cambios en los datos comunes compartidos.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="cc2b7-106">La señalización fuera de banda es más eficaz cuando se usa en combinación con un mecanismo de control de versiones, lo que permite al asociado detectar el cambio para notificar a los asociados remotos la versión de los datos compartidos que se debe esperar.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="cc2b7-107">Volviendo al ejemplo de RPC proporcionado en la sección "sesgo de la versión" del comportamiento de la [replicación en Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), el servidor RPC podría volver a llamar a los clientes conectados para informarles del traslado a un nuevo servidor: "voy a mover.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="cc2b7-108">Por lo tanto, la replicación le llevará la nueva dirección en breve "para que el cliente pueda controlar el período de transición.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="cc2b7-109">Las aplicaciones que requieren directivas idénticas para que se puedan comunicar entre sí pueden utilizar la señalización fuera de banda para asegurarse de que no se emplea una nueva Directiva hasta que todas las partes implicadas la hayan recibido.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="cc2b7-110">Por ejemplo, si se cambia la Directiva del Protocolo de seguridad de Internet (IPsec) entre dos equipos, un agente en el equipo de origen podría ponerse en contacto con un agente en el equipo de destino para negociar la aplicación de la directiva modificada, con la aplicación que retrasa la máquina de origen hasta que la máquina de destino haya recibido también la nueva Directiva.</span><span class="sxs-lookup"><span data-stu-id="cc2b7-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




