---
title: Compruebe que el servidor es quien dice ser
description: Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776111"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="c3e51-103">Compruebe que el servidor es quien dice ser</span><span class="sxs-lookup"><span data-stu-id="c3e51-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="c3e51-104">Es mejor usar la autenticación mutua y, por tanto, comprobar la identidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="c3e51-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="c3e51-105">Un ejemplo de un error común que no se puede hacer es las aplicaciones que tienen un servicio local en el que los clientes llaman.</span><span class="sxs-lookup"><span data-stu-id="c3e51-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="c3e51-106">En algunas configuraciones, un administrador puede decidir que el servicio de sistema de no es realmente útil y puede optar por detenerlo.</span><span class="sxs-lookup"><span data-stu-id="c3e51-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="c3e51-107">Un atacante inventive en un equipo de Terminal Server puede iniciar un proceso que escucha en el mismo punto de conexión y, cuando un cliente se conecta a un punto de conexión, lo que permite la suplantación en el servidor sin autenticar mutuamente el servidor, el atacante puede suplantar al cliente y obtener acceso a los datos del cliente o realizar llamadas de red en nombre del cliente</span><span class="sxs-lookup"><span data-stu-id="c3e51-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="c3e51-108">La mayoría de los servicios del sistema se ejecutan con una cuenta conocida, como LocalSysyem, LocalService o NetworkService, que se puede comprobar mediante la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="c3e51-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




