---
title: Niveles de autenticación
description: Microsoft RPC proporciona varios niveles de autenticación.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268726"
---
# <a name="authentication-levels"></a><span data-ttu-id="d4e3e-103">Niveles de autenticación</span><span class="sxs-lookup"><span data-stu-id="d4e3e-103">Authentication Levels</span></span>

<span data-ttu-id="d4e3e-104">Microsoft RPC proporciona varios niveles de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="d4e3e-105">Según el nivel de autenticación, se puede comprobar el origen del tráfico (que la entidad de seguridad envió el tráfico) cuando se establece la conexión, cuando el cliente inicia una nueva llamada a procedimiento remoto o durante cada intercambio de paquetes entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="d4e3e-106">Incluso cuando se comprueba el remitente del tráfico, la seguridad sigue siendo débil, puesto que dicha comprobación no garantiza que el paquete no se haya modificado o dañado en la ruta. solo comprueba que el paquete procede de la entidad de seguridad especificada.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="d4e3e-107">Para mayor seguridad, las aplicaciones distribuidas pueden establecer la biblioteca en tiempo de ejecución de RPC para comprobar que no se modifica ninguno de los datos intercambiados entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="d4e3e-108">La biblioteca RPC también puede cifrar el contenido de cada paquete antes de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="d4e3e-109">En general, las aplicaciones que desean proteger su tráfico deben usar solo los dos últimos niveles: integridad y privacidad.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="d4e3e-110">Tenga en cuenta que los niveles más altos de autenticación requieren una mayor sobrecarga computacional.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="d4e3e-111">Usted, como desarrollador, debe decidir cuál es más importante para su aplicación (velocidad o seguridad).</span><span class="sxs-lookup"><span data-stu-id="d4e3e-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="d4e3e-112">La mayoría de los desarrolladores encontrarán que, con algunas pruebas de rendimiento, pueden alcanzar niveles de rendimiento aceptables y mantener la seguridad adecuada.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="d4e3e-113">Las partes del cliente y del servidor de la aplicación distribuida deben usar el mismo nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="d4e3e-114">Para obtener una lista de los niveles de autenticación RPC, vea [constantes de nivel de autenticación](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4e3e-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




