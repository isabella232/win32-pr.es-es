---
title: Publicación de servicios
description: Los servicios se anuncian mediante objetos almacenados en Active Directory Domain Services.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- AD de publicación de servicio
- Active Directory, uso, publicación de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075100"
---
# <a name="service-publication"></a><span data-ttu-id="b9470-105">Publicación de servicios</span><span class="sxs-lookup"><span data-stu-id="b9470-105">Service Publication</span></span>

<span data-ttu-id="b9470-106">Los servicios se anuncian mediante objetos almacenados en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b9470-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="b9470-107">Esto se conoce como *publicación de servicio*.</span><span class="sxs-lookup"><span data-stu-id="b9470-107">This is known as *service publication*.</span></span> <span data-ttu-id="b9470-108">Los clientes consultan el directorio para encontrar los servicios.</span><span class="sxs-lookup"><span data-stu-id="b9470-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="b9470-109">Esto se denomina *cliente-servicio Rendezvous*.</span><span class="sxs-lookup"><span data-stu-id="b9470-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="b9470-110">En esta sección se describen los tipos de objetos de directorio que se usan para la publicación de servicio y se explica cómo se usan para el encuentro de servicio de cliente.</span><span class="sxs-lookup"><span data-stu-id="b9470-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="b9470-111">En esta sección se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b9470-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="b9470-112">Información general de la publicación de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="b9470-113">Problemas de seguridad para la publicación de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="b9470-114">Objetos de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="b9470-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="b9470-115">Publicación con puntos de conexión de servicio (SCP)</span><span class="sxs-lookup"><span data-stu-id="b9470-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="b9470-116">Información que se va a almacenar en un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="b9470-117">Dónde crear un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="b9470-118">Publicación de servicios replicables, basados en host y de base de datos mediante puntos de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="b9470-119">Crear y mantener un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="b9470-120">Cómo un cliente consulta un SCP y lo usa para enlazar a una instancia de servicio</span><span class="sxs-lookup"><span data-stu-id="b9470-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="b9470-121">Uso de las API del servicio de nombres de RPC (RpcNs) para publicar un servicio RPC</span><span class="sxs-lookup"><span data-stu-id="b9470-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="b9470-122">Registro y resolución de Windows Sockets (RnR) para publicar un servicio de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b9470-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="b9470-123">Publicación de servicios basados en COM en el almacén de clases COM+</span><span class="sxs-lookup"><span data-stu-id="b9470-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="b9470-124">Para obtener más información sobre cómo se autentican los servicios y los clientes entre sí, vea [autenticación mutua mediante Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="b9470-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="b9470-125">Para obtener más información sobre los contextos de seguridad del servicio y las cuentas de inicio de sesión, consulte [cuentas de inicio de sesión del servicio](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="b9470-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




