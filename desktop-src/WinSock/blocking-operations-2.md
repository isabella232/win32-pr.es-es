---
description: La noción de bloqueo en un entorno de Windows ha sido históricamente muy importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696404"
---
# <a name="blocking-operations"></a><span data-ttu-id="3f8d6-103">Operaciones de bloqueo</span><span class="sxs-lookup"><span data-stu-id="3f8d6-103">Blocking Operations</span></span>

<span data-ttu-id="3f8d6-104">La noción de bloqueo en un entorno de Windows ha sido históricamente muy importante.</span><span class="sxs-lookup"><span data-stu-id="3f8d6-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="3f8d6-105">En entornos Windows Sockets 1,1, no se recomiendan las llamadas de bloqueo, ya que solían deshabilitar la interacción continua con el sistema.</span><span class="sxs-lookup"><span data-stu-id="3f8d6-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="3f8d6-106">Además, emplean una técnica pseudoblocking que, por diversos motivos, no siempre funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="3f8d6-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="3f8d6-107">Sin embargo, en entornos de Windows programados de forma preventiva, las llamadas de bloqueo tienen mucho más sentido, pueden ser implementadas por los servicios del sistema operativo nativo y, en realidad, son un mecanismo preferido.</span><span class="sxs-lookup"><span data-stu-id="3f8d6-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="3f8d6-108">La API de Winsock 2 ya no es compatible con psuedoblocking, pero debido a que las correcciones de compatibilidad de Windows Sockets 1,1 deben seguir emulando este comportamiento, los proveedores de servicios deben admitir esto tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="3f8d6-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



