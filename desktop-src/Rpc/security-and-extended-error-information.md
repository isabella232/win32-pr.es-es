---
title: Seguridad e información de error ampliada
description: La información de error extendida ofrece datos muy útiles a la hora de solucionar problemas de RPC, pero muchos de ellos se consideran confidenciales en las organizaciones con seguridad.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779087"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="21757-103">Seguridad e información de error ampliada</span><span class="sxs-lookup"><span data-stu-id="21757-103">Security and Extended Error Information</span></span>

<span data-ttu-id="21757-104">La información de error extendida ofrece datos muy útiles a la hora de solucionar problemas de RPC, pero muchos de ellos se consideran confidenciales en las organizaciones con seguridad.</span><span class="sxs-lookup"><span data-stu-id="21757-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="21757-105">En consideración de estos problemas de seguridad, la información de error ampliada está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="21757-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="21757-106">La información de error extendida se sigue generando cuando la información de error extendida está deshabilitada, pero la información nunca se transmite a través de los límites de proceso o equipo.</span><span class="sxs-lookup"><span data-stu-id="21757-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="21757-107">Este enfoque permite que la información de errores sea utilizada por herramientas que tienen acceso al espacio de direcciones de proceso, como depuradores.</span><span class="sxs-lookup"><span data-stu-id="21757-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="21757-108">Cuando está activada, se genera información de error extendida que se puede enviar a través de los límites del proceso y del equipo.</span><span class="sxs-lookup"><span data-stu-id="21757-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="21757-109">Actualmente, la información de error extendida se usa para las secuencias de protocolos orientados a conexiones y RPC local (LRPC).</span><span class="sxs-lookup"><span data-stu-id="21757-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="21757-110">Se implementa parcialmente para los datagramas.</span><span class="sxs-lookup"><span data-stu-id="21757-110">It is partially implemented for datagrams.</span></span>

 

 




