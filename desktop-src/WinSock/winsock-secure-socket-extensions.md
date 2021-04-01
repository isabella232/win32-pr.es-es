---
description: Las extensiones de sockets seguros para Winsock permiten a una aplicación de socket controlar la seguridad de su tráfico a través de una red.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensiones Winsock Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082110"
---
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="3b431-103">Extensiones Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="3b431-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="3b431-104">Las extensiones de sockets seguros para Winsock permiten a una aplicación de socket controlar la seguridad de su tráfico a través de una red.</span><span class="sxs-lookup"><span data-stu-id="3b431-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="3b431-105">Estas extensiones permiten a una aplicación proporcionar los requisitos y la Directiva de seguridad para el tráfico de red y consultar la configuración de seguridad aplicada.</span><span class="sxs-lookup"><span data-stu-id="3b431-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="3b431-106">Por ejemplo, una aplicación puede utilizar estas extensiones para consultar el token de seguridad del mismo nivel que se puede usar para realizar comprobaciones de acceso de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b431-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="3b431-107">Las extensiones de sockets seguros están diseñadas para integrar los servicios proporcionados por IPsec y otros protocolos de seguridad con el marco Winsock.</span><span class="sxs-lookup"><span data-stu-id="3b431-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="3b431-108">Antes de Windows Vista, en Windows Server 2003 y Windows XP, un administrador ha configurado IPsec a través de directivas locales y de dominio.</span><span class="sxs-lookup"><span data-stu-id="3b431-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="3b431-109">En Windows Vista, las extensiones de sockets seguros permiten a las aplicaciones configurar por completo o parcialmente y controlar la seguridad del tráfico de red en el nivel de socket.</span><span class="sxs-lookup"><span data-stu-id="3b431-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="3b431-110">Las aplicaciones ya pueden proteger el tráfico de red mediante el uso de API públicas, como la administración de IPsec, la plataforma de filtrado de Windows y la interfaz del proveedor de compatibilidad para seguridad (SSPI).</span><span class="sxs-lookup"><span data-stu-id="3b431-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="3b431-111">Sin embargo, el uso de estas API puede dificultar el desarrollo de la aplicación y hacer que sea más difícil de configurar e implementar.</span><span class="sxs-lookup"><span data-stu-id="3b431-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="3b431-112">Las extensiones Winsock Secure Socket se han diseñado para simplificar el desarrollo de aplicaciones de red que requieran tráfico de red seguro, ya que permiten a Winsock administrar la mayor parte de la complejidad.</span><span class="sxs-lookup"><span data-stu-id="3b431-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="3b431-113">Estas extensiones de sockets seguros están disponibles en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b431-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="3b431-114">Funciones de socket seguro</span><span class="sxs-lookup"><span data-stu-id="3b431-114">Secure Socket Functions</span></span>

<span data-ttu-id="3b431-115">Las funciones de extensión de sockets seguros son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b431-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="3b431-116">**WSADeleteSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="3b431-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="3b431-117">**WSAImpersonateSocketPeer**</span><span class="sxs-lookup"><span data-stu-id="3b431-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="3b431-118">**WSAQuerySocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="3b431-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="3b431-119">**WSARevertImpersonation**</span><span class="sxs-lookup"><span data-stu-id="3b431-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="3b431-120">**WSASetSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="3b431-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="3b431-121">**WSASetSocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="3b431-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="3b431-122">Actualmente, las funciones de socket seguro solo admiten el protocolo IPsec y están disponibles en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b431-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="3b431-123">Las estructuras y enumeraciones utilizadas por las funciones de sockets seguros son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b431-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="3b431-124">**\_nombre de \_ destino del mismo nivel de socket \_**</span><span class="sxs-lookup"><span data-stu-id="3b431-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="3b431-125">**\_Protocolo de seguridad de socket \_**</span><span class="sxs-lookup"><span data-stu-id="3b431-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="3b431-126">**\_información de \_ consulta de seguridad de socket \_**</span><span class="sxs-lookup"><span data-stu-id="3b431-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="3b431-127">**\_plantilla de \_ consulta de seguridad de socket \_**</span><span class="sxs-lookup"><span data-stu-id="3b431-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="3b431-128">**\_configuración de seguridad de socket \_**</span><span class="sxs-lookup"><span data-stu-id="3b431-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="3b431-129">**configuración de seguridad de SOCKETs \_ \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="3b431-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="3b431-130">Las funciones de sockets seguros son fáciles de usar para las aplicaciones normales y son lo suficientemente flexibles para las aplicaciones que necesitan un alto grado de control sobre la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3b431-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="3b431-131">Estas funciones permiten mantener oculto el mecanismo de seguridad subyacente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b431-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="3b431-132">Una aplicación puede especificar los requisitos de seguridad genéricos y dejar que el administrador controle el protocolo de seguridad que se usa para admitir los requisitos.</span><span class="sxs-lookup"><span data-stu-id="3b431-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="3b431-133">Aunque es posible extender estas funciones para agregar otros protocolos de seguridad, actualmente solo IPsec se integra con las funciones de socket seguro.</span><span class="sxs-lookup"><span data-stu-id="3b431-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="3b431-134">La función [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permite a una aplicación habilitar la seguridad y aplicar la configuración de seguridad antes de que se establezca una conexión.</span><span class="sxs-lookup"><span data-stu-id="3b431-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="3b431-135">La función [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permite a una aplicación especificar el nombre de destino correspondiente a una entidad del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="3b431-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="3b431-136">El protocolo de seguridad seleccionado usará esta información al autenticar al mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="3b431-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="3b431-137">Esta característica soluciona los problemas de ataques de tipo "Man in the Middle".</span><span class="sxs-lookup"><span data-stu-id="3b431-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="3b431-138">La función [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) se usa para eliminar un nombre del mismo nivel especificado previamente para un socket.</span><span class="sxs-lookup"><span data-stu-id="3b431-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="3b431-139">Una vez establecida una conexión, la función [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permite que una aplicación consulte las propiedades de seguridad de la conexión, que pueden incluir el acceso del mismo nivel o el token de acceso al equipo.</span><span class="sxs-lookup"><span data-stu-id="3b431-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="3b431-140">Una vez establecida una conexión, la función [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permite a una aplicación suplantar la entidad de seguridad correspondiente a un socket del mismo nivel para realizar la autorización en el nivel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b431-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="3b431-141">[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permite a una aplicación finalizar la suplantación de un socket del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="3b431-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="3b431-142">Arquitectura de sockets seguros</span><span class="sxs-lookup"><span data-stu-id="3b431-142">Secure Socket Architecture</span></span>

![arquitectura básica de las extensiones Winsock Secure Socket](images/ss-arch.png)

-   <span data-ttu-id="3b431-144">Una aplicación llama a las funciones de socket seguro para establecer o consultar la configuración de seguridad de un socket.</span><span class="sxs-lookup"><span data-stu-id="3b431-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="3b431-145">Las funciones de socket seguro son un conjunto de funciones de extensión con seguridad de tipos que encapsulan llamadas a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con valores recién definidos para el parámetro *DwIoControlCode* disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b431-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="3b431-146">Estos ioctl se controlan por la pila de red.</span><span class="sxs-lookup"><span data-stu-id="3b431-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="3b431-147">La pila de red dirigirá la llamada a la aplicación de [capa de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md) junto con el identificador de extremo.</span><span class="sxs-lookup"><span data-stu-id="3b431-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="3b431-148">En el caso de las funciones [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)y [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , Ale configurará la configuración de la aplicación en el punto de conexión local.</span><span class="sxs-lookup"><span data-stu-id="3b431-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="3b431-149">En el caso de la función [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , Ale leerá la información solicitada de los puntos de conexión locales y remotos aplicables.</span><span class="sxs-lookup"><span data-stu-id="3b431-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="3b431-150">En función de los eventos de socket, el cumplimiento del nivel de aplicación (ALE) aplica directivas para la arquitectura de sockets seguros mediante la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="3b431-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="3b431-151">Para obtener más información, vea [acerca de la plataforma de filtrado de Windows](../fwp/about-windows-filtering-platform.md) y el [cumplimiento del nivel de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md).</span><span class="sxs-lookup"><span data-stu-id="3b431-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b431-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b431-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b431-153">Acerca de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="3b431-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="3b431-154">Ejemplos avanzados de Winsock con extensiones de socket seguras</span><span class="sxs-lookup"><span data-stu-id="3b431-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="3b431-155">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="3b431-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="3b431-156">Configuración de IPsec</span><span class="sxs-lookup"><span data-stu-id="3b431-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="3b431-157">Funciones de IPsec</span><span class="sxs-lookup"><span data-stu-id="3b431-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="3b431-158">Programación de Winsock segura</span><span class="sxs-lookup"><span data-stu-id="3b431-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="3b431-159">Interfaz del proveedor de compatibilidad con seguridad (SSPI)</span><span class="sxs-lookup"><span data-stu-id="3b431-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="3b431-160">Uso de extensiones de socket seguras</span><span class="sxs-lookup"><span data-stu-id="3b431-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="3b431-161">Plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="3b431-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="3b431-162">Funciones de la API de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="3b431-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 
