---
title: Autenticación mutua con Kerberos
description: La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente antes de que se transmita el tráfico de la aplicación a través de la conexión del cliente o servicio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, autenticación mutua
- Active Directory, uso, seguridad, autenticación mutua
- seguridad AD
- seguridad AD, autenticación mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656331"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="a86e1-107">Autenticación mutua con Kerberos</span><span class="sxs-lookup"><span data-stu-id="a86e1-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="a86e1-108">La autenticación mutua es una característica de seguridad en la que un proceso de cliente debe demostrar su identidad a un servicio y el servicio debe demostrar su identidad al cliente antes de que se transmita el tráfico de la aplicación a través de la conexión del cliente o servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="a86e1-109">Active Directory Domain Services y Windows proporcionan compatibilidad con los nombres principales de servicio (SPN), que son un componente clave en el mecanismo de Kerberos mediante el cual un cliente autentica un servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="a86e1-110">Un SPN es un nombre único que identifica una instancia de un servicio y está asociado a la cuenta de inicio de sesión en la que se ejecuta la instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="a86e1-111">Los componentes de un SPN son de tal forma que un cliente puede crear un SPN para un servicio sin la cuenta de inicio de sesión del servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="a86e1-112">Esto permite al cliente solicitar al servicio que autentique su cuenta, aunque el cliente no tenga el nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a86e1-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="a86e1-113">En esta sección se incluye información general sobre:</span><span class="sxs-lookup"><span data-stu-id="a86e1-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="a86e1-114">Autenticación mutua mediante Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a86e1-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="a86e1-115">Crear un SPN único.</span><span class="sxs-lookup"><span data-stu-id="a86e1-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="a86e1-116">Cómo registra un instalador de servicio los SPN en el objeto de cuenta asociado a una instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="a86e1-117">Cómo una aplicación cliente usa el objeto de punto de conexión de servicio (SCP) de una instancia de servicio en Active Directory Domain Services para recuperar datos de los que se va a crear un SPN para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="a86e1-118">Cómo una aplicación cliente usa un SPN de servicio junto con la interfaz del proveedor de compatibilidad para seguridad (SSPI) para autenticar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a86e1-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="a86e1-119">Un ejemplo de código para una aplicación de cliente o servicio de Windows Sockets que usa un SCP y SSPI para realizar la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="a86e1-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="a86e1-120">Un ejemplo de código para un cliente o servicio RPC que realiza la autenticación mutua mediante el servicio de nombres RPC y la autenticación RPC.</span><span class="sxs-lookup"><span data-stu-id="a86e1-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="a86e1-121">Cómo un servicio de registro y resolución de Windows Sockets (RnR) usa SPN para realizar la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="a86e1-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="a86e1-122">En esta sección se describe el uso de Dominio de Active Directory servicio para la autenticación mutua, en particular, el propósito de los puntos de conexión de servicio y los nombres de entidad de seguridad de servicio en la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="a86e1-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="a86e1-123">No es un debate completo sobre cómo usar SSPI para la autenticación mutua o la compatibilidad de autenticación y seguridad disponible para las aplicaciones RPC y Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a86e1-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="a86e1-124">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="a86e1-124">For more information, see:</span></span>

-   [<span data-ttu-id="a86e1-125">Publicar con puntos de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="a86e1-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="a86e1-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="a86e1-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="a86e1-127">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a86e1-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="a86e1-128">RPC</span><span class="sxs-lookup"><span data-stu-id="a86e1-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 