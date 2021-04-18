---
description: Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticación implícita de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648561"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="0cdc0-103">Autenticación implícita de Microsoft</span><span class="sxs-lookup"><span data-stu-id="0cdc0-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="0cdc0-104">Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="0cdc0-105">El servidor comprueba que el cliente no se ha autenticado y, a continuación, realiza la autenticación inicial mediante el acceso a los servicios de un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="0cdc0-106">Para obtener una descripción detallada de este procedimiento, vea [autenticación inicial mediante Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="0cdc0-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="0cdc0-107">Cuando la autenticación inicial se realiza correctamente, el servidor recibe una [*clave de sesión*](../secgloss/s-gly.md)de resumen.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0cdc0-108">El servidor almacena en caché esta clave y la usa para autenticar las solicitudes posteriores de recursos del cliente.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="0cdc0-109">Esta autenticación es local, es decir, no requiere acceso a un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="0cdc0-110">Para obtener una descripción detallada de este procedimiento, consulte [autenticación de solicitudes posteriores mediante Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="0cdc0-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="0cdc0-111">Cuando se usa HTTP, no se mantiene ninguna conexión entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="0cdc0-112">Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, Microsoft Digest almacena en caché la información recibida después de la autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="0cdc0-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="0cdc0-113">Para obtener información sobre este proceso, vea [mantener el contexto de seguridad entre conexiones](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="0cdc0-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
