---
title: Conceder el derecho de inicio de sesión como servicio en el equipo host
description: Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773147"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="68e82-103">Conceder el derecho de inicio de sesión como servicio en el equipo host</span><span class="sxs-lookup"><span data-stu-id="68e82-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="68e82-104">Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="68e82-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="68e82-105">Tenga en cuenta que este derecho de inicio de sesión solo se aplica al equipo local y debe concederse en la Directiva LSA local de cada equipo host.</span><span class="sxs-lookup"><span data-stu-id="68e82-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="68e82-106">Este paso no es necesario si el servicio se ejecuta como LocalSystem, que, de forma predeterminada, se concede a este derecho.</span><span class="sxs-lookup"><span data-stu-id="68e82-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="68e82-107">Para obtener más información sobre cómo conceder el derecho de inicio de sesión como servicio mediante programación, consulte el [código de ejemplo LSAPrivs](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="68e82-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




